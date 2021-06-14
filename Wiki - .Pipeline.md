### 1. Shortlist Drug/Condition

- read the csvfiles.  In this instance we are selecting the BNFCode prefix '0403' which represents anti-depressants

import pandas

BNF_SECTION='0403'

GPdata=pandas.read_csv(path.join('data','GPData202006',"GPData202006.csv"),header=0)

AddressData=pandas.read_csv(path.join('data','GPData202006',"Address.csv"),header=0)

BNFData=pandas.read_csv(path.join('data','GPData202006',"BNF.csv"),header=0)

ChemSubstance=pandas.read_csv(path.join('data','GPData202006',"ChemSubstance.csv"),header=0)

GPdata_filtered=GPdata[GPdata.BNFCode.str.startswith(BNF_SECTION)]

### 2. Investigate longitudinal data

- select one or a sample of the shortlisted drugs based on a particular variable i.e. cost/quantity.  Pull historic data for the selection and visualise the data.  Data is available from April 2012 for GP prescription data in Wales (April 2016 for hospital prescribing (primary care only)).

_sample code to be posted here_

### 3. Select Drug/Condition for text/API search

- from the visualised data in point 2, look to select one or two drugs that show unbalanced historical data, a significant difference in cost, or a significant difference in amount prescribed.

_sample code to be posted here_

### 4. Add the drug name(s) to a PubMed/PMC API search and return abstracts

- from the output in point 3, add the named drugs to the following API's.  This will return the paper codes, which will in turn return the abstracts.

https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pubmed&term=pioglitazone&reldate=60&datetype=edat&retmax=100

https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pubmed&id=32914429,32912770

https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=pubmed&id=32914429,32912770&rettype=abstract&retmode=text

https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esearch.fcgi?db=pmc&term=pioglitazone&reldate=30&datetype=edat&retmax=100

https://eutils.ncbi.nlm.nih.gov/entrez/eutils/esummary.fcgi?db=pmc&id=7480213,7477453

https://eutils.ncbi.nlm.nih.gov/entrez/eutils/efetch.fcgi?db=pmc&id=7480213,7477453

https://dataguide.nlm.nih.gov/eutilities/utilities.html

### 5. Complete sentiment analysis on the returned abstracts

- use NLP process to determine the sentiment of the returned abstracts for the chosen drug(s).  Although sentiment analysis will not necesarily influence a review of the EBM, a strong negative sentiment would prompt further investigation.

_sample code to be posted here_

### 6. Extract relevant data from the abstracts

- return an output per abstract which confirms the study population, methods, results and conclusion.  In time we will look to complete an abstractive summary of the abstract, but in the first instance, we will return an extractive summary.  Population should return a positive number, and the other headers should return a small sentence of no more than 15 words.

_sample code to be posted here_

### 7. Manually edit motion graphic template with extractive summary

- created in Adobe.

_sample code to be posted here_
