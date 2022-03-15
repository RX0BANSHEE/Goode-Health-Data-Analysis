# Goode-Health-Data-Analysis
Introduction

With the improvement of living standards, people pay more and more attention to health. Accordingly, many companies provide health assistance to customers through remote monitoring, implementation supervision, dietary guidance and other methods. 
My sponsor, Goode health, supplies customers with customized super food mixtures by analyzing the content of important biomarkers in customers' blood, so as to reduce the occurrence of diseases and maintain health. The data set is provided by the Goode Health 2021 year of customer’s records in a CSV format containing both numeric value and categorical value. The original data set contains 1365 observations and 15 variables with missing values. After cleaning the data and fixing the missing value, the new data we would use for further analysis is with 1789 observations, the variables we would use in the further analysis are, gender, state, cholesterol, LDL, triglycerides, hs_ CRP, HbA1c, HDL, customer age, Cholesterol_ HDL ratio, triglycerides_ HDL ratio. Note that the last two columns were created manually, it is the ratio of cholesterol and HDL, and the ratio of triglycerides and HDL. To make it easy for the analysis, we replaced the “MALE” with numeric value “1” and replaced the “FEMALE” with numerical value “0”, so all the values will be numeric in our new data set except the state.

The goal of this project is to learn more about the health status of customers by analyzing the data set, and to establish a model to predict the comprehensive health indicators of customers. In the exploratory analysis part, data visualization, such as the distribution of cholesterol and the distribution of LDL, directly displays the relationship and changes between variables, and statistical tests are performed to verify whether there are differences between men and women in the content of various biomarkers. A linear regression model is established to predict the comprehensive health indicators of customers using Python.

Business Questions

1. How do our customers health status look like ?

2. Any differences between age, gender or region ?

3. Which index it is the key to evaluate customers’ health?

4. Can we predict customers’ health conditions via blood test result?

Methodology

In this group project, there will be three parts the analysis:
1.	Data processing & cleaning: joining original and updated raw dataset; delete duplicate value; delete or correct error value; imputing null value and fixing outlier.
2.	EDA: conducting the exploratory data analysis along with data visualization (histogram, bar plots, scatter plots, maps, etc).
3.	Predictive modeling: data labeling, regression model construction, classifier model construction.


Limitation

First, the data set is not balanced since the number of female observations is more than the male observation. Second, the size of the data set is relatively small, it will be hard in resampling the data to make it balanced due to the limited observations. Third, more information of customers should be provided to fully evaluate the health status, such as BMI.

Conclusion

Based on the exploratory data analysis above, we can conclude that most of our customers’ biomarkers stay at the average level. A young woman usually has lower cholesterol, LDL, and higher HDL levels than a man. The hs_ CRP level will increase with age for both males and females. Most of the biomarkers in this data set have correlations with each other. The average age of male customers is different from the average age of female customers in each state and in general, the average age of male customers in each state is greater than that of female customers. From 25 to 80 years old, the average cholesterol content of each age group is not different, but there is a huge difference between the 80-85 age group and the 85-90 age group. The health risk indicators of both male and female customers has a normal distribution. The number of customers with health risk indicators in the range [8,10)is the largest.

After modeling to predict customer Healthy Index and Risk Level, we found that Linear Regression model is good at to predict Healthy Index and Random Forest Classifier is good to predict Risk level. These models also found hs_CRP level and HDL_Level is crucial index to evaluate customer healthy conditions. In the end, those 2 predictive models crate a access to help sponsor categories the customer that provide further customize services to the market.



Package used
numpy
pandas
os
matplotlib
missingno
seaborn
sklearn








