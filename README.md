# Diabetes Prediction Model

## Overview
This project develops and compares various machine learning models to predict diabetes based on health metrics from the National Health and Nutrition Examination Survey (NHANES) dataset. The models classify individuals into three categories based on their glycohemoglobin (HbA1c) levels:
- Normal (HbA1c < 5.7%)
- Prediabetes (5.7% ≤ HbA1c ≤ 6.4%)
- Diabetes (HbA1c ≥ 6.5%)

## Dataset
The analysis uses data from multiple NHANES datasets:
- Demographic information
- Laboratory results
- Examination measurements
- Diet information
- Health questionnaire responses

## Data Preprocessing
The preprocessing pipeline includes:
- Merging multiple data sources
- Handling missing values
- Feature selection and engineering
- Converting glycohemoglobin levels to diabetes classification labels

## Features Used
The final model uses these key features:
- Gender
- Years in US (binary)
- Family income
- Arm circumference
- Sagittal abdominal diameter
- Grip strength
- Breastfeeding history

## Models Implemented
Several machine learning algorithms were implemented and compared:
1. Logistic Regression
2. AdaBoost with Decision Tree base
3. Bagging with Decision Tree base
4. Bagging with K-Nearest Neighbors
5. Multi-Layer Perceptron (Neural Network)

## Results
The models achieved the following accuracy scores on the test set:
- MLP: 78.44%
- Logistic Regression: 78.36%
- Bagging with KNN: 78.34%
- Bagging with Decision Tree: 76.58%
- AdaBoost: 64.49%

The MLP classifier with a (100, 50) hidden layer architecture performed the best, though the difference between the top three models is minimal.

## Requirements
- Python 3.x
- pandas
- numpy
- matplotlib
- seaborn
- scikit-learn

## Usage
To run the model:
```python
# Import the file
from diabetes_prediction_model import *

# Train the model with your own data
# X_train, y_train = your_data
# model.fit(X_train, y_train)

# Make predictions
# predictions = model.predict(X_test)
```

