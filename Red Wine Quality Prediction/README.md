# Red Wine Quality Prediction

## Introduction

For this project, I used Kaggle’s Red Wine Quality dataset to build various classification models to predict whether a particular red wine is “good quality” or not. Each wine in this dataset is given a “quality” score between 0 and 10. For the purpose of this project, I converted the output to a binary output where each wine is either “good quality” (a score of 6.5 or higher) or not (a score below 6.5). The quality of a wine is determined by 11 input variables:
1. Fixed acidity
2. Volatile acidity
3. Citric acid
4. Residual sugar
5. Chlorides
6. Free sulfur dioxide
7. Total sulfur dioxide
8. Density
9. 	pH
10. Sulfates
11. Alcohol

## Objectives
The objectives of this project are as follows
1. To experiment with different classification methods to see which yields the highest accuracy
2. To determine which features are the most indicative of a good quality wine

## Setup
First, I imported all of the relevant libraries that I’ll be using as well as the data itself.

## Understanding Data
Next, I wanted to get a better idea of what I was working with.
There are a total of 1599 rows and 12 columns. The data looks very clean by looking at the first five rows, but I still wanted to make sure that there were no missing values.

## Missing Values
This is a very beginner-friendly dataset. I did not have to deal with any missing values, and there isn’t much flexibility to conduct some feature engineering given these variables. Next, I wanted to explore my data a little bit more.

## Exploring Variables
Bar plot of ‘quality’ variable
first, Compare all 11 input variable with quality to find out which are related.

## Preparing Data for Modelling
Standardizing Feature Variables
At this point, I felt that I was ready to prepare the data for modelling. The first thing that I did was standardize the data using pipeline. Standardizing the data means that it will transform the data so that its distribution will have a mean of 0 and a standard deviation of 1. It’s important to standardize your data in order to equalize the range of the data.

## Making binary classificaion for the response variable
Dividing wine as good and bad by giving the limit(6.5) for the quality columns.
##Label Encoder
I use LabelEncoder() for converting catergorical data of quality good and bad wrt 1 and 0

## Split data
Next I split the data into a training and test set so that I could cross-validate my models and determine their effectiveness.

## Modelling
For this project, I wanted to compare three different machine learning models: Random Forest Classifier, Stochastic Gradient Descent Classifier and  Support Vector Classifier(SVC). For the purpose of this project, I wanted to compare these models by their accuracy using pipeline

## Result 
Random Forest Classifier gives high accuracy compare to others

## Conclusion
By looking into the details, we can see that good quality wines have higher levels of alcohol on average, have a lower volatile acidity on average, higher levels of sulphates on average, and higher levels of residual sugar on average.
