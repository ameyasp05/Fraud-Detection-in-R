# Fraud Detection in R

# Overview

This project focuses on predicting credit card fraud using various machine learning algorithms. The dataset used contains transactions made by credit cards in September 2013 by European cardholders. The goal is to distinguish fraudulent transactions from legitimate ones using various classification algorithms and evaluate their performance.

# Prerequisites

Make sure that the following libraries are installed in your R environment. These can be installed using the install.packages() function.

# Required Libraries:

caret
rpart
xgboost
dplyr
randomForest
rpart.plot
pROC
ROSE
neuralnet

You can install these packages by running the following commands:

#Install required libraries
install.packages("caret")
install.packages("rpart")
install.packages("xgboost")
install.packages("dplyr")
install.packages("randomForest")
install.packages("rpart.plot")
install.packages("pROC")
install.packages("ROSE")
install.packages("neuralnet")

Once installed, the libraries can be loaded using the following:

#Load required libraries
library(caret)
library(rpart)
library(dplyr)
library(ROSE)
library(randomForest)
library(rpart.plot)
library(xgboost)
library(neuralnet)

# Dataset

The dataset (creditcard.csv) contains 31 columns where the Class column represents the target variable, with 1 indicating fraud and 0 indicating a legitimate transaction. The dataset is heavily imbalanced, with the vast majority of transactions being legitimate.

# Data Processing

Data Viewing and Structure: The dataset is loaded and explored using functions like View(), str(), and head().

Handling Missing Values: The dataset is checked for any missing values using sum(is.na()). No missing values are assumed.

Class Conversion: The Class variable is converted into a factor for classification.

# Data Visualization

Density Plots: Density plots are created to visualize frauds vs. non-frauds based on transaction Time and Amount.
Pie Chart: A pie chart is created to compare the proportion of fraudulent and non-fraudulent transactions.

# Data Splitting
 
The dataset is shuffled and split into training (80%) and testing (20%) sets. The test set is further split into input features (credit_card.test) and target labels (credit_card.testc).

# Models Implemented

The following machine learning models are implemented:

Logistic Regression:
A logistic regression model is trained using the glm() function.
Performance is evaluated using confusion matrix and ROC curve.
Decision Tree:
A decision tree classifier is built using rpart() and visualized using rpart.plot().
Model performance is evaluated using confusion matrix and ROC curve.
Random Forest:
A random forest model is built using the randomForest() function with 39 trees and other hyperparameters.
Performance is evaluated using confusion matrix and ROC curve.
XGBoost:
An XGBoost classifier is built using xgboost().
Model performance is evaluated using confusion matrix and ROC curve.
Artificial Neural Network:
An artificial neural network (ANN) model is trained using the neuralnet() function.
The performance is evaluated using the computed results from the test data.

# Model Evaluation

For each model, performance metrics such as accuracy, confusion matrix, and ROC curve are used for evaluation. The final results show that the XGBoost model performs the best, with an accuracy score of 99.96% and an AUC of 0.910.

# Conclusion

This project implements and compares multiple machine learning algorithms for detecting credit card fraud. The XGBoost algorithm was found to be the most effective, identifying the majority of fraudulent transactions with high accuracy.

# Files

creditcard.csv: The dataset used for fraud detection.
fraud_detection.R: The main R script containing the code for preprocessing, model training, and evaluation.

# References

Dataset source: Kaggle Credit Card Fraud Detection Dataset
