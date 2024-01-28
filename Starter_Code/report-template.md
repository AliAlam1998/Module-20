# Module 12 Report Template

# Loan Risk Prediction Analysis Report

## Overview of the Analysis

### Purpose:
The purpose of this analysis was to develop machine learning models for predicting loan risks based on given financial information. The goal was to assist in identifying healthy loans (0) and high-risk loans (1) to support informed decision-making in the lending process.

### Data Information:
The dataset used for analysis contained financial information on loan applicants, including features such as income, debt, employment status, and more. The target variable was 'loan_status,' which had two classes: '0' indicating a healthy loan and '1' indicating a high-risk loan.

### Stages of Machine Learning Process:
1. **Data Preprocessing:** Handled missing values, encoded categorical variables, and scaled numerical features.
2. **Labeling:** Created labels set (`y`) from the 'loan_status' column and features set (`X`) from remaining columns.
3. **Exploratory Data Analysis:** Reviewed the distribution of loan classes using `value_counts`.
4. **Data Splitting:** Split the dataset into training and testing sets.
5. **Model Training:** Utilized logistic regression models with original and resampled data.
6. **Evaluation:** Calculated accuracy, generated confusion matrices, and printed classification reports.

### Methods Used:
- Logistic Regression: Developed initial models using logistic regression for loan risk prediction.
- Random OverSampling: Implemented resampling techniques to address class imbalance in the dataset.

## Results
### Machine Learning Model 1: Logistic Regression with Original Data
- **Balanced Accuracy:** 0.99
- **Confusion Matrix:** [[14947 64][ 47 450]]
- **Classification Report:**
            precision    recall  f1-score   support
0           1.00      1.00      1.00     15011
1           0.88      0.91      0.89       497
accuracy    0.99      0.99      0.99     15508
### Machine Learning Model 2: Logistic Regression with Resampled Data
- **Balanced Accuracy:** 1.00
- **Confusion Matrix:** [[14938 73][ 2 495]]
- **Classification Report:**
            precision    recall  f1-score   support
0           1.00      1.00      1.00     15011
1           0.87      1.00      0.93       497
accuracy    1.00      1.00      1.00     15508

## Summary

The logistic regression model with resampled data demonstrates superior performance, achieving a balanced accuracy score of 1.00. This indicates a perfect balance between sensitivity and specificity. The model is effective at predicting both healthy and high-risk loans, as evidenced by high precision, recall, and F1-score values for both classes.

**Recommendation:**
The logistic regression model trained with resampled data is recommended for predicting loan risks due to its outstanding performance across various evaluation metrics. The model is well-suited for scenarios where accurate identification of both healthy and high-risk loans is crucial.

