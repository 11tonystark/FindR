# Recession Predictor with Factor affecting Financial Crisis

This repository contains code & documentation for a data wrangling group project on the multiple dataset **Financial Data** (https://fred.stlouisfed.org) (https://stats.oecd.org/Index.aspx?DataSetCode=MEI_CLI) (https://www.nber.org/research/business-cycle-dating) (https://www.eia.gov) (https://www.macrohistory.net/database/) (https://pitchbook.com/data).

**Team Members**
1. Tanmay Shukla - Mentor and Developer 
2. Hong Ye - SQL, Python, Data Prediction and Manipulation 
3. Miaomiao Fu - Excel, Financial Analysis, Data Visualization 
4. Mingliang Ge - Research Analysis, Python, Data Cleaning 
5. Xiaoqing Xia - R, Modelling, Data Wrangling 

**Our Approaches**

1. Data Collection Using Webscraping
2. Cleaning Dataset using Microsoft Excel
3. Feature Slection 
4. Financial Analysis
5. Developing a models for Financial Crisis Prediction.
6. Implementation of Stock Simulator 

**Documentation**
1. Pipeline-FindR.pdf 
2. Detail Explanation of our Project 

**Introduction**
Financial crises have significant implications for the lives of billions of people. Bad economic decisions during the financial recession can cause people's assets to shrink. Our goal is to predict the likelihood of another recession in the future using the two recessions we have experienced. Also, it is to help us make more accurate financial decisions when we know exactly when the recession will occur and how long it will last, such as investing in stocks at the lowest point and avoiding entering the stock market during the economic downturn. Spotting their warning signs early can facilitate the timely activation of countermeasures to prevent them. 

**Data Description**
We grabbed the following four data lists from the FRED website via the API key, as they were too complex and heavy, so R Studio helped us to present them directly in software and clean them up further.
FRED
(1). 10-Year Treasury Constant Maturity Minus 3-Month Treasury Constant Maturity
(2). Job Openings (Monthly), Seasonally Adjusted
(3). Business Tendency Surveys for Manufacturing: Confidence Indicators: Composite Indicators: OECD Indicator for the United States (Federal Reserve Bank of St. Louis)
(4). NBER based Recession Indicators for the United States from the Period following the Peak through the Trough (USREC)

EIA (U.S. Energy Information Administration)
(1). Electric Power Monthly
And we also download the data from Nasdaq, Yahoo, Pitchbook and OECD.. 

We put all the downloaded datasets and API key data into Python and found some missing values in the official statistics, two of which are important indicators for our recession study: 10-Year and 3-month Treasury Constant Maturities. 

Our dataset contains 250 features and 150 countries in a time span from 1970 to 2021. After feature selection, we have 27 key features. Among these key features, there are three features that contain some value missing. To make the model perfect, we use the financial model to predict the values for three financial data in Excel. Then we replace the missing value with the values from the financial models. 

We do most of our data processing in Python as well as Excel, so we don't use SQL very much. We collected data from a private company, Crunchbase Inc., for changes between 2016 and 2021 and imported it into SQL. 

**Methods**
The main purpose of the project is to find the key features of recession in the United States. Firstly, we use the regression model to predict the recession and figure out the different significant features for 150 countries that can contribute to the financial crisis. Secondly, we use the feature selection method to obtain the key features that can cause financial crises which only work in the United States. From all the features, we have 27 key features for our model. To persuade the significant features of the model by using feature selection, we use the SHAP value, which is used to assign each feature an importance value for a particular prediction.

Then we list the factors that are important to the US based on these features: predict financial crisis and recession, logistic regression, random forest  decision trees and XGboost. We will know which feature affects the most. After we found all the key factors that determine recession, predict financial crisis and recession, logistic regression, random forest decision trees, and XGboost gave us the weight of each factor in our determination of recession.

After machine learning modeling, we already get the probability of recession. However, it’s never enough to get this, the important factor is time is still missing, so we still don’t know when the recession will come. Here comes the time series. After we get those features, we use LSTM, exponential smoothed recurrent neural networks (α-RNNs)  method  for forecasting. We find the dataset from different time duration. Next step is to go back and clean the dataset so that it makes the dataset monthly. After that,  we add one dataset from time to the LSTM method to predict the recession time. 

**Conclusion**
With the data we have now and the models we have built, we have very good evidence to conclude that we are in a recession. However, there are very many limitations to our study. Firstly, there are so many datasets, so we need to drop many datasets, do better cleaning and design more precise models. We need to use more computational power to train the dataset. Also, the more tests will help us in the selection of features. Secondly, because the change in the financial market is so fast, if we want to make the prediction more precisely we need to update the data frequently.	



**Libraries Used**

1. tidytext
2. seaborn
3. requests
4. pandas
5. wordcloud2
6. Keras
7. dplyr
8. tidyr
9. ggplot2
10. Tensorflow
11. Sklearn
12. Math
13. re
14. yfinance 
15. Seaborn, Pandas, Numpy, tqdm

**Folder Description**
1. Main Model - Recession Predicton and Simulator -  Use ReadME file to run the code 
2. Recession Indicator Using ANN - Use ReadME file to run the code 
3. Recession Prediction using R -  Use ReadME file to run the code 


**Languages Used**

1. [R Programming](https://www.r-project.org/about.html) - Used for Data Visualization and Ml Modeling .
2. [Python3](https://www.python.org/download/releases/3.0/) - Used for Financial Crisis Prediction and Classification of Factor That can cause Financial Crisis.
3. [Microsoft Excel](https://www.microsoft.com/en-us/microsoft-365/excel) - Primary tool for cleaning and Prediction of our Finance Data.
