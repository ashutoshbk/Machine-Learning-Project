# Human Activity Recognition with Smartphones

## Introduction

The dataset used for this paper is from the [UCI Machine Learning Repository](https://archive.ics.uci.edu/ml/datasets/Human+Activity+Recognition+Using+Smartphones) titled “Smartphone-Based Recognition of Human Activities and Postural Transitions Data Set” (SBHAR). The data was collected from experiments with a group of 30 volunteers aged between 19 to 48 years wearing a Samsung Galaxy SII on the waist. Volunteers performed a protocol of activities including six basic postures: three static — standing, sitting, lying and three dynamic — walking, walking downstairs and walking upstairs. 


## Setup
First, I imported all of the relevant libraries that I’ll be using as well as the data itself.

## Understanding Data
Next, I wanted to get a better idea of what I was working with.
There are a total of 7352 rows and 563 columns in training and 2947 rows and 563 in testing with the last column as Activity which will act as our label. The data looks very clean by looking at the first five rows, but I still wanted to make sure that there were no missing values.

## Dataset Exploration
### Which Features Are There?
The features seem to have a main name and some information on how they have been computed attached. Grouping the main names will reduce the dimensions for the first impression.

Mainly there are 'acceleration' and 'gyroscope' features. A few 'gravity' features are there as well. Impressive how many features there are in regard of the limited number of sensors used.

### Missing Values
This is a very accurate dataset. I did not have to deal with any missing values, and there isn’t much flexibility to conduct some feature engineering given these variables. Next, I wanted to explore my data a little bit more.

### Let's See How Are The Labels Distributed?
With the Bar chart you can how labels are distribute.


## Activity Exploration
### Are The Activities Separable?
Here, I first scale the data with StandardScaler() then reduce the dimension with Principal component analysis and Transform data with t-distributed stochastic neighbor embedding.

I got,
	1. In plot 1 you can clearly see the activities are mostly separable.
	2. Plot 2 reveals personal information of the participants. Everybody has for example an unique/sparable walking style (on the upper right). Therefore the smartphone should be able to detect what you are doing and also who is using the smartphone (if you are moving around with it).

### How Good Are The Activities Separable?
Without much preprocessing and parameter tuning a simple LGBMClassifier should work decently.

With a basic untuned model the activity of the smartphone user can be predicted with an accuracy of 95%.
This is pretty striking regarding six equally distributed labels.


### Summary:
If the smartphone or an App wants to know what you are doing, this is feasible.