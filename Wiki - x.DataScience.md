## DS Process

#### Load
1.       Libraries / head / describe (basic familiarity with structure)
         - import pandas as pd
         - import numpy as np
         - import matplotlib.pyplot as plt
         - import seaborn as sns
         - %matplotlib inline

         Get Data
         - df = pd.read_csv('fooFile.csv')
         - df = pd.read_csv('fooFile.csv', index_col=0)
         - pd.read_excel('Excel_Sample.xlsx',sheetname='Sheet1')
         - df = pd.read_html('http://www.fdic.gov/bank/individual/failed/banklist.html')

         Info
         - fooDF.info()   #returns columns, non-null counts, dtype

2.       Sum / std dev / max / mean / value_count / sort / groupby (basic familiarity with data)

#### EDA
1.       Countplot of target field (chart)
2.       Histogram of other relevant fields (chart)
3.       Corr() of all data (table)
4.       Corr() as heatmap (chart)
5.       Scatter plot of data that looks correlated (chart)
6.       Boxplot target variable against str column (chart)
7.       Calc/group summary stats (describe())
8.       Look at unique values
9.       Countplot of unique values (with hue)
10.       Closer look countplot at interesting values (chart)
11.       Create new col(s) to split values into 0 and 1 across columns
12.       Bar plot showing corr() amongst features (chart)
Alternative - joint plot / lmplot / hist / pairplot / kde plot / facetgrid / rug plot / factor plot / pair grid

#### Data/pre-processing
1.       Count missing values / as % per col
2.       Unique operations
3.       Get rid of duplicate/pointless cols/outliers
4.       For nulls, look to see what can be correlated.
5.       Fill in nulls with corr() or delete out low if low %
6.       Create dummy variables (drop originals)
7.       Get rid of pointless bits of fields (i.e day and month if only need year)
8.       Standardise/normalise the variables (scaler, esp NN)
9.       NLP – requires additional steps (punc/stopwords/tokenize/stem/vectorise etc)

#### Models
1.       X and Y and Test/train split (include linear, logistic, KNN, decision tree classifier, SVM, NLP, (No test train split required for K-means/PCA/recommender systems)
2.       Normalise data
3.       Create model
4.       Fit model to training data (train data)
5.       Save model
6.       Evaluate – metrics and matrix (classification report) / plot loss vs val-loss / MSE, MAE, RMSE

·         K-value (plot, choose value, retrain)

·         Support vector machine (grid search)

·         Tensorflow (add layers, drop out layers, early stopping)
