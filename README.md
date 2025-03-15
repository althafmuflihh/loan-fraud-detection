# Loan Fraud Classification with Logistic Regression

## Project Objective
This project aims to develop a logistic regression model to classify loan fraud cases based on user characteristics and loan activities. The model is optimized using class balancing and feature engineering, with performance evaluated through accuracy, precision, recall, F1-score, and Average Precision (AP).

## Methods Used
* Machine Learning
* Logistic Regression
* Data Preprocessing & Feature Engineering

## Evaluation Metrics
* Accuracy
* Precision
* Recall
* F1-score
* Average Precision Score

## Language
* Python

## Modules Used
* Pandas
* NumPy
* Sklearn

## Step-by-Step Process

1. **Dataset Analysis & Preprocessing**
    * Check class distribution (fraud vs. non-fraud)
    * Handle missing values

2. **Data Balancing & Sampling**
    * Sample non-fraud cases to balance the dataset

3. **Feature Engineering**
    * Create new features:
        * loan_count: Number of loans taken
        * loan_recent: Most recent loan timestamp

4. **Data Preparation**
    * Remove unnecessary columns
    * Standardize numerical features

5. **Model Training**
    * Split data into train-test (80:20 split, stratified)
    * Train logistic regression model

6. **Hyperparameter Tuning**
    * Adjust class_weight='balanced' for handling class imbalance
    * Increase max_iter=1000 for better convergence

7. **Model Evaluation**
    * **Metric** | **Training Data** | **Test Data**
        * Accuracy | 76.11% | 75.87%
        * Average Precision (AP) | - | 0.706

    * **Classification Report (Test Data)**
        * **Class** | **Precision** | **Recall** | **F1-Score** | **Support**
            * Non-Fraud (0) | 0.85 | 0.72 | 0.78 | 4190
            * Fraud (1) | 0.66 | 0.81 | 0.72 | 2735

    * **Macro Average**: 
        * Precision = 0.75, Recall = 0.77, F1-score = 0.75

    * **Weighted Average**: 
        * Precision = 0.77, Recall = 0.76, F1-score = 0.76

## Results
Scored 0.03932 and ranked 46th out of 222 in the leaderboard of the RISKEK Datathon 2024 competition
