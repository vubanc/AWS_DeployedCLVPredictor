# AWS_DeployedCLVPredictor
Customer Lifetime Value (CLV) is a metric that represents the net profit/revenue that a company can generate from a certain customer. Predicting CLV can assist a company to decide what campaigns should be directed to the customer. For instance, for customers with low lifetime values, a company may attempt to increase spending. And for customers with high lifetime values, the company may focus more on retention. 

This is an end-to-end machine learning project completed using Amazon Web Services (AWS). In this project, a UK Online Retail dataset (e-commerce dataset) consisting of 500,000 transactions (from 1800 customers) was used to predict customer lifetime values. The project can be subdivided into 3 sections. The 3 sections are:

- Data Cleaning and Preprocessing (**Data Wrangling.ipynb**): Perfromed feature engineering, imputed outliers using KNN, standardized the data, segmented customers into 2 CLV categories (response label) using K-means clustering, uploaded the data to S3 buckets.
- Data Querying (**Data Querying.ipynb**): Performed bivariate analysis by running SQL queries on Amazon Athena.
- CLV Prediction and Model Deployment (**AWS_DeployedCLVPredictor.ipynb**): Predicted CLV as a regression problem using an econometric model, predicted CLV category (low or high) of customers using XGBoost, boosted the accuracy of the XGBoost model using RandomizedSearchCV, deployed the XGBoost model to a sagemaker REST endpoint and tested the deployed model.
