Following Phase 1 of this project (where we have tracked down and made sense of the medical literature), we will need to consider how the current best evidence is reflected in the GP prescription data.  

GP prescription data for Wales is available to download via http://www.primarycareservices.wales.nhs.uk/general-practice-prescribing-data-extrac.  

The Welsh GP prescription data is split into 4 tables that cover the GP address, GP prescription data, the chemical within the drug, and the British National Formulary (BNF) prescribed drug description.

The prescription data is published on a monthly basis and covers prescriptions that are prescribed in Wales by GP's and non medical prescribers that have prescribed on behalf of the GP practice, that are then dispensed in the community within Wales or England. The data includes all prescribed medicines, dressings and appliances that are dispensed each month. If a patient does not take a prescription to the pharmacy for dispensing, then the information will not be included in the dataset. Private prescriptions are not included in the data.

The first step is to clean the data.  The GP address data included duplicates that needed to be removed (this would have formed many-to-many relationships which most RDB's do not like).  The data analysis was done in Access as PowerBI had problems querying the size of the data files.  In addition, duplicate 'BNFChemical' codes were removed from the ChecmSubstance table.  The entity diagram for the 4 tables is as follows;

![GP entity diagram (2)](https://user-images.githubusercontent.com/45914355/83583230-af3ebf80-a53b-11ea-8346-9cae53fc5412.png)

We were then able to run queries that extracted the following data points;
- The sum and combined cost of individual prescriptions
- The sum and combined costs of prescriptions by high level disorder
- The sum and combined costs of prescriptions by specific disorder
- The sum and combined costs of prescription by GP practice

Queries were moved to PowerBI for further analysis.  Respectively, a cut of the **February 2020** data for the 4 queries listed above is shown below;

![Feb20 IndividualDrugData (2)](https://user-images.githubusercontent.com/45914355/83693253-a8708500-a5ed-11ea-9def-00a06e9b66c5.png)

SELECT GPData202002v2.BNFName, BNF.SectionDesc, Sum(GPData202002v2.Items) AS SumOfItems, Sum(GPData202002v2.ActCost) AS SumOfActCost, [SumOfActCost]/[SumOfItems] AS Expr1

FROM GPData202002v2 INNER JOIN BNF ON GPData202002v2.BNFChemical = BNF.BNFChemical

GROUP BY GPData202002v2.BNFName, BNF.SectionDesc

ORDER BY Sum(GPData202002v2.ActCost) DESC;

![Feb20 GpPrescriptionHLDisorder (2)](https://user-images.githubusercontent.com/45914355/83693632-5ed46a00-a5ee-11ea-998a-df0a17dce3d0.png)

SELECT BNF.ChapterDesc, Sum(GPData202002v2.ActCost) AS SumOfActCost, Sum(GPData202002v2.Items) AS SumOfItems, [SumOfActCost]/[SumOfItems] AS CostPerItem

FROM BNF INNER JOIN GPData202002v2 ON BNF.BNFChemical = GPData202002v2.BNFChemical

GROUP BY BNF.ChapterDesc

ORDER BY Sum(GPData202002v2.ActCost) DESC;

![Feb20 GpPrescriptionLLDisorder (2)](https://user-images.githubusercontent.com/45914355/83693850-c8ed0f00-a5ee-11ea-8df3-0e4e6c8c5c2b.png)

SELECT GPData202002v2.BNFChemical, BNF.ChapterDesc, Sum(GPData202002v2.ActCost) AS SumOfActCost, Sum(GPData202002v2.Items) AS SumOfItems

FROM GPData202002v2 INNER JOIN BNF ON GPData202002v2.BNFChemical = BNF.BNFChemical

GROUP BY GPData202002v2.BNFChemical, BNF.ChapterDesc

ORDER BY Sum(GPData202002v2.ActCost) DESC;

![Feb20PrescriptionsBySurgery (2)](https://user-images.githubusercontent.com/45914355/83693951-06519c80-a5ef-11ea-9e07-b7360c464bbd.png)
SELECT GPData202002v2.HB, GPData202002v2.PracticeID, Address_DupsRemoved.Street, Address_DupsRemoved.Posttown, Sum(GPData202002v2.ActCost) AS SumOfActCost, Sum(GPData202002v2.Items) AS SumOfItems, [SumOfActCost]/[SumOfItems] AS Expr1

FROM BNF INNER JOIN (([ChemSubstance DupsRemoved] INNER JOIN GPData202002v2 ON [ChemSubstance DupsRemoved].BNFChemical = GPData202002v2.BNFChemical) INNER JOIN Address_DupsRemoved ON GPData202002v2.PracticeID = Address_DupsRemoved.PracticeId) ON BNF.BNFChemical = [ChemSubstance DupsRemoved].BNFChemical

GROUP BY GPData202002v2.HB, GPData202002v2.PracticeID, Address_DupsRemoved.Street, Address_DupsRemoved.Posttown;

### Visualisation example - Pioglitazone

Pioglitazone is medication used to treat diabetes.  It is often used where Metformin is not recommended or cannot be used.  However, studies have highlighted the negative side effects of Pioglitazone, and as reported on https://bnf.nice.org.uk/drug/pioglitazone.html, can increase the risk of heart failure.  

Using the GP prescription data to plot the location (surgery postcode) and the sum of Pioglitazone prescriptions for the 4 health boards in south-east Wales, we can visualise any outliers.

![Pioglitazone Map (2)](https://user-images.githubusercontent.com/45914355/83822702-b3004c80-a6c9-11ea-8deb-e5b4e8842a8b.png)

From the image above we can see an outlier east of Swansea, and to a lesser degree, an outlier north of Pontypridd.  The image below shows Pioglitazone prescriptions by postal town, locality, and health board. I haven't included a legend, but the locality and HB codes are available online.  For the moment we just want to get a sense of what the GP data for Wales can tell us.  But ultimately, the analysis of the data will be directed by the output from the Phase 1 deliverable (i.e EBM summarisation and paraphrasing).  The Welsh GP data is available from 2013 to date.

![Pioglitazone Data](https://user-images.githubusercontent.com/45914355/83826858-e1375980-a6d4-11ea-8c92-e83927c5f87a.png)

To consider (and consider longitudinal, how outliers have performed over time, vs hospital prescribing)...
- Does the EBM suggest that one drug is no better than another, yet a prescribed drug, for a particular practice, is far more expensive.
- Does the cost of a certain type of drug make up a large % of the total spend for that practice (compared to peers, per drug, groups)
- Does the EBM suggest that a particular drug has side effects in a particular cohort.
- Cost vs prescribed vs strength of EBM (Gapminder).
- Consider centiles, outliers, PU(prescribing unit)
