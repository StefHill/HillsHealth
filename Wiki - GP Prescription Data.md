Following Phase 1 of this project where we have tracked down and made sense of the medical literature, we will need to consider how the current best evidence is reflected in the GP prescription data.

GP prescription data for Wales is free and available to download via http://www.primarycareservices.wales.nhs.uk/general-practice-prescribing-data-extrac.  

The data is split into 4 tables that cover the GP address, GP prescription data, the British National Formulary (BNF) prescribed drug description, and the chemical within the drug.

The prescription data is published on a monthly basis and the data covers prescriptions that are prescribed in Wales by GP's and non medical prescribers that have prescribed on behalf of the GP practice, that are then dispensed in the community within Wales or England. The data includes all prescribed medicines, dressings and appliances that are dispensed each month. If a patient does not take a prescription to the pharmacy for dispensing, then the information will not be included in the dataset. Private prescriptions are not included in the data.

The first step was to clean the data.  The GP address data included duplicates that needed to be removed (this would have formed many-to-many relationships which most RDB's do not like).  The data munging was done in Access as PowerBI had problems querying the size of the data files.  In additon, duplicate 'BNFChemical' codes were removed from the ChecmSubstance table.  The entity diagram for the 4 tables is as follows;

![GP entity diagram (2)](https://user-images.githubusercontent.com/45914355/83583230-af3ebf80-a53b-11ea-8346-9cae53fc5412.png)

The 
