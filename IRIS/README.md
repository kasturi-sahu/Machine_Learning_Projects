# Machine Learning on IRIS Data Set

![](https://github.com/kasturi-sahu/Machine_Learning_Projects/blob/main/IRIS/Iris%20Setosa.png)

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

Iris is a genus of 260–300 species of flowering plants with showy flowers. Iris is also widely used as a common name for all Iris species. Iris is extensively grown as ornamental plant in home and botanical gardens. The Iris flowers color ranges from white, pink, orange, purple, lavender.

## Description of Data

There are almost 300 different species of Iris has been already discoverd, for our Data Science purpose we are going to make EDA for following 3 different Iris species:

1. Setosa
2. Versicolor
3. Virginica

The flowers are classified by the features

1. sepal lenght in cm
2. sepal width in cm
3. petal length in cm
4. petal width in cm

![](https://github.com/kasturi-sahu/Machine_Learning_Projects/blob/main/IRIS/0_7H_gF1KnslexnJ3s.png)

## Summary Of the Data
- We have 150 rows and 5 columns. 
- 1 column is the name of the species (object data type)
- There are 4 columns showing the sepal length, sepal width, petal length and petal width (float data type)
- There is no missing or null data
- As expected only the species is an object type
- Other columns have float data

## Handling Duplciate Rows
- After removing the duplicate values, we have 147 Rows and 5 Columns

## Handling Outlier
- We can clear see that there are number of black dots in "sepal_width" column which are referring to the outliers, so it means the data in this column are outside the distribution
- The second step is to remove the outliers, there are different way to remove the outliers that are find the IQR, Zscore values

## Z Score 
- We find the zscore value and then we have decided to make one threshold value as 3 which is standard of industry recommend value
- We removed all the outliers which zscore value is greater than 3
- After removing the outlier finally there are 146 rows and 5 columns presents in the data set.

## Skewness
- We first calculated the skew value and all of the column skew value are near to zero
- The best skew value for normally distribution is very close to zero
- Making the skewness value near to zero will help to get better score

## Label Encoding
- We have converted Species Column to numerical form

## Machine Learning (Model Building)
### Model Building and Finding Difference of Cross Validation from R2 & RMSE
- We have used 5 models for Model Building
- We have used 5 Evaluation Techniques
- We have evaluated the difference between R2 and Cross Validation. Also, the difference between RMSE and Cross Validation
- The best way to select a model is to have high R2 and low RMSE
- Random Forest and Decission Tree have high R2 and low RMSE
- Also, the difference between R2 and Cross Validation and the difference between RMSE and Cross Validation is low in case of Random Forest and Kneighbor Model

## Hyper Parameter Tuning

- Hyper Parameter Tuning on the Feature Engineered Model, has improved for all
- Random Forest is the highest which is 100.0

## Conclusion
- We have built 5 models
- We have used F1score, precision, recall 
- Also, to avoid over fitting and under fiitng issues, we have used Cross Validation
- We have chosen the best model and done hyper Parameter tuning on it, to improve the performance
- Hyper Tuning was done on 3 models
- As per the evaluation with (80:20) training and testing data Random Forest is the best model
- The accuracy for Random Forest is 100%



**Please find the notebook [here](https://github.com/kasturi-sahu/Machine_Learning_Projects/blob/main/IRIS/Iris%20Flower%20Dataset.ipynb "here")**





