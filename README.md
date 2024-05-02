# Absenteeism Data Analysis

This repository contains code for analyzing absenteeism data to predict whether an employee will be absent from work for more than the median time.

## Introduction

The analysis focuses on preprocessing the dataset and building a predictive model using logistic regression. Various preprocessing steps are performed, including one-hot encoding for the reason for absence, grouping reasons, transforming the target variable, and feature engineering.

## Dataset

The dataset includes the following columns:

- ID
- Reason for Absence
- Date
- Transportation Expense
- Distance to Work
- Age
- Daily Work Load Average
- Body Mass Index
- Education
- Children
- Pets
- Absenteeism Time in Hours

## Preprocessing Steps

1. **One-Hot Encoding for Reason for Absence:**
   - Categorical feature 'Reason for Absence' is encoded using one-hot encoding.
   - One category is dropped to avoid multicollinearity.

2. **Grouping Reasons for Absence:**
   - Remaining reasons are grouped into four categories for simplification.

3. **Target Variable Transformation:**
   - 'Absenteeism Time in Hours' is transformed into two categories:
     - 0 if hours absent are less than or equal to the median time.
     - 1 otherwise.

4. **Feature Engineering:**
   - Employee ID column is discarded.
   - Date column is processed to extract month and day of the week.
   - Date column is then removed.

## Proposed Model

A logistic regression model is proposed for the analysis due to its effectiveness in predicting binary outcomes. The model will be trained on the preprocessed dataset to predict the probability of an employee being absent for more than the median time.
