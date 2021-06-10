# Machine Learning on Bank DataSet

## Summarization of Learning

### 9 steps of EDA
- Define Problem
- Choose right tools
- Collection of data
- Pre-profile
- Pre processing of data (Clean, remove unnecessary, add relevant data)
- Post-profile
- Ask right Questions
- Conclusion or Summarization
- Actionable Insights (low hanging fruits)

### 7 Stages of ML
- Data Collection
- Data Preparation
- Choose Model
- Train Model
- Evaluate Model
- Improve Model
- Predict Model

## Introduction
### Problem Statement

We will consider the Interest Rate as output variable and predict the best model to fit.

## Summary Of the Data
- We have 2499 rows and 14 columns. 
- There are 7 Float data type, 6 Integer data type and 1 Object data type
- There are some null values in some of the column
- Only the FICO.Range is an object data type

## Handling Duplciate Rows
- There are no duplicate values, we have 2499 Rows and 14 Columns

## Handling Null Values
- After dropping the null values, we have 2484 Rows and 14 Columns

## Handling Outlier
- From above image we can clear see that there are number of black dots in most of the column which are referring to the outliers, so it means most of the data are outside the distribution.
- The second step is to remove the outliers, there are different way to remove the outliers that are find the IQR, Zscore values.

## Z Score 
- We find the zscore value and then we have decided to make one threshold value as 3 which is standard of industry recommend value
- We removed all the outliers which zscore value is greater than 3
- After removing the outlier finaily there are 2358 rows and 13 columns presents in the data set

## Skewness
- We first calculated the skew value and some of the column skew value are far from zero
- The best skew value for normally distributes is very close to zero, so we are using “log1p” method to make the skew value near to zero
- In the last cell I am again checking the skewness value and there is difference between the first skewness value and second, now the skewness value of each column is near to zero
- Making the skewness value near to zero will help to get better score

## Label Encoding
- We have converted FICO.Range Column to numerical form

## Correlation with Variable
- We have seen multiple ways to check the co-relation with the target varialbe
- The last graph makes it very clear that "Monthly.Income" is close to 0 co-relation
- All the Features have positive or a negative co-relation 

## Machine Learning (Model Building)
### Model Building and Finding Difference of Cross Validation from R2 & RMSE
- We have used 7 models for Model Building
- We have used 5 Evaluation Techniques
- We have evaluated the difference between R2 and Cross Validation. Also, the difference between RMSE and Cross Validation
- The best way to select a model is to have high R2 and low RMSE
- Random Forest have high R2 and low RMSE
- Also, the difference between R2 and Cross Validation and the difference between RMSE and Cross Validation is low in case of Random Forest Model
- We will use Gradient boosting model for our model tuning

### Feature Engineering- Model building by removing low co-related column
- After dropping one column, our score for Gradient boost has not improved 
- So for the same reasons (High R2 and low RMSE) we are choosing Gradient boost again for our Hyperparameter tuning
- We will also take Random Forest for Hyperparameter tuning

## Hyper Parameter Tuning
- Hyper Parameter Tuning on the Feature Engineered Model, has improved for all 
- Gradient Boosting Regressor is the highest which is 0.87

## Conclusion
- After loading the data properly, we found that it had a lot of “NAN” values. So, we removed the “NAN” values
- From further analysis we found it is a Regression data set
- After removing the “NAN” values, few columns which were not required were dropped
- We had to do Label Encoding for few columns
- Outliers handled applying Zscore and Skewness through log transformation
- Model Building Was done in 2 ways after finding the Best Random state
- In Model 1, we have used 7 models and 5 Evaluation Techniques. Also, we have found the difference between R2 and Cross Validation, RMSE and Cross Validation and found Gradient Boosting Regressor Model is the best model
- In Model 2, we have used Feature Engineered by dropping a column for which the co-relation was close to “0”. And we found an improvement for Gradient Boosting Regressor Model
- Hyper Tuning was done on 2 models
- As per the evaluation with (80:20) training and testing data Gradient Boosting Regressor model is the best model
- Gradient Boosting Regressor is the highest which is 0.87

**Please find the notebook [[here](http://https://github.com/kasturi-sahu/Machine_Learning_Projects/blob/main/Bank%20Dataset/Bank%20Dataset.ipynb "here")]**




