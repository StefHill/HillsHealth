### 1. Shortlist Drug/Condition

import pandas

BNF_SECTION='0403'

- read the.csvfiles

GPdata=pandas.read_csv(path.join('data','GPData202006',"GPData202006.csv"),header=0)

AddressData=pandas.read_csv(path.join('data','GPData202006',"Address.csv"),header=0)

BNFData=pandas.read_csv(path.join('data','GPData202006',"BNF.csv"),header=0)

ChemSubstance=pandas.read_csv(path.join('data','GPData202006',"ChemSubstance.csv"),header=0)

GPdata_filtered=GPdata[GPdata.BNFCode.str.startswith(BNF_SECTION)]
