# Machine Learning on Avocado Data Set
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

Avocado is a fruit consumed by people heavily in the United States.

This data was downloaded from the Hass Avocado Board website in May of 2018 & compiled into a single CSV.

The table below represents weekly 2018 retail scan data for National retail volume (units) and price. Retail scan data comes directly from retailer's cash registers based on actual retail sales of Hass Avocados.

Starting in 2013, the table below reflects an expanded, multi-outlet retail data set. Multi-outlet reporting includes an aggregation of the following channels: grocery, mass, club, drug, dollar and military. The Average Price (of avocados) in the table reflects as per unit (per avocado) cost, even when multiple units (avocados) are sold in bags.

The Product Lookup codes (PLU’s) in the table are only for Hass avocados. Other varieties of avocados (e.g. greenskins) are not included in this table.

Some relevant columns in the dataset:

|ID|Feature|Description|
|:--|:--|:--|
|01|Date| The date of the observation| 
|02|AveragePrice| The average price of a single Avocado | 
|03|type| Conventional or organic| 
|04|year| The year|
|05|Region| The city or region of the observation |
|06|Total Volume| Total number of avocados sold|
|07|4046| Total number of avocados with PLU 4046 sold|
|08|4225| Total number of avocados with PLU 4225 sold|
|09|4770| Total number of avocados with PLU 4770 sold|

**Inspiration /Label**

Our task is to make a mode that can consider the data provided and predict the Average Price.

## Description of Data

- There are 18249 rows and 14 columns
- Therev are 2 Types of Avocados
- There are no missing values
- There are 9 Float, 2 Integer and 3 Object columns

## Handling Outlier

- We can see that there are number of black dots in most of the column which are referring to the outliers, so it means most of the data are outside the distribution.

- The second step is to remove the outliers, there are different way to remove the outliers that are find the IQR, Zscore values.

## Z Score 
- We find the zscore value and then we have decided to make one threshold value as 3 which is standard of industry recommend value
- We removed all the outliers which zscore value is greater than 3
- After removing the outlier finally there are 17651 rows and 14 columns presents in the data set.

## Skewness
- We first calculated the skew value and see some of the column skew value are far from zero
- The best skew value for normally distribution is very close to zero, so we used “log1p” method to make the skew value near to zero
- Making the skewness value near to zero will help to get better score

## Label Encoding
We have converted Region, Year  and Type to numerical form

## Dropping Date, Month and Day Column
We have removed Date, Month and Day column

## Machine Learning (Model Building)
### Model Building and Finding Difference of Cross Validation from R2 & RMSE

- We have used 7 models for Model Building
- We have used 5 Evaluation Techniques
- We have evaluated the difference between R2 and Cross Validation. Also, the difference between RMSE and Cross Validation
- The best way to select a model is to have high R2 and low RMSE
- Random Forest have high R2 and low RMSE
- Also, the difference between R2 and Cross Validation and the difference between RMSE and Cross Validation is low in case of Random Forest Model
- We will use Random Forest model for our model tuning

### Feature Engineering- Model building by removing low co-related column

- After dropping one column, our score for Random forest has not improved 
- So for the same reasons (High R2 and low RMSE) we are choosing Random Forest again for our Hypermodel tuning

## Hyper Parameter Tuning

- Hyper Parameter Tuning on the Feature Engineered Model, has improved for all
- Random Forest is the highest which is 0.85

## Conclusion

- After loading the data properly, we found that it had a lot of “NAN” values. So, we removed the “NAN” values
- From further analysis we found it is a Regression data set
- After removing the “NAN” values, few columns which were not required were dropped
- We had to do Label Encoding for few columns
- Outliers handled applying Zscore and Skewness through log transformation
- Model Building Was done in 2 ways after finding the Best Random state
- In Model 1, we have used 7 models and 5 Evaluation Techniques. Also, we have found the difference between R2 and Cross Validation, RMSE and Cross Validation and found Random Forest Model is the best model
- In Model 2, we have used Feature Engineered by dropping a column for which the co-relation was close to “0”. And we found an improvement for Random Forest Model
- Hyper Tuning was done on 3 models
- As per the evaluation with (80:20) training and testing data Random Forest is the best model



**Please find the notebook [here](http://https://github.com/kasturi-sahu/Machine_Learning_Projects/blob/main/Avocado/Machine%20Learning%20on%20Avocado%20Data%20Set.ipynb "here")**





