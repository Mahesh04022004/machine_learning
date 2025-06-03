🔷 What is Normalization?

Normalization means scaling your data values so that they all fall in a similar range, usually between 0 and 1.

    📌 Think of normalization like resizing all your data values to be on the same scale — this helps ML models understand the data better.

🔷 Why Normalize Data?

Let’s say you have the following data:
Feature	Value Range
Age	0 – 100
Salary	10,000 – 200,000
Height (cm)	100 – 200

The problem is: Salary dominates other values because of its big scale. Some ML algorithms give more importance to large values unless all features are on the same scale.
⚠️ Without Normalization:

    Algorithms like KNN, SVM, or Gradient Descent perform poorly.

    The model gets biased toward higher-range features.

🔷 How Normalization Works
Formula:

Normalized Value = (X−Min)/(Max−Min)(X−Min)/(Max−Min)

It scales all data between 0 and 1.
Example:

Suppose we have a feature called Age:
Age (Original)	Min = 10	Max = 60	Normalized Value
10			(10-10)/(60-10) = 0.0
30			(30-10)/(60-10) = 0.4
60			(60-10)/(60-10) = 1.0
🔷 Types of Normalization (or Feature Scaling)
1. Min-Max Normalization

    Scales features between 0 and 1

    Use when the data is not normally distributed

from sklearn.preprocessing import MinMaxScaler
scaler = MinMaxScaler()
scaled_data = scaler.fit_transform(data)

2. Z-Score Standardization (Standard Scaling)

    Converts data to have mean = 0 and standard deviation = 1

    Best for Gaussian (normal) distribution

from sklearn.preprocessing import StandardScaler
scaler = StandardScaler()
standardized_data = scaler.fit_transform(data)

3. Robust Scaler

    Uses median and IQR (interquartile range) instead of mean/std

    Good for datasets with outliers

from sklearn.preprocessing import RobustScaler
scaler = RobustScaler()
robust_scaled_data = scaler.fit_transform(data)

🔷 Which Machine Learning Models Need Normalization?
Model Type	Needs Normalization?	Why?
KNN (K-Nearest Neighbors)	✅ Yes	Uses distance between points
SVM (Support Vector Machines)	✅ Yes	Sensitive to data scale
Linear Regression	✅ Often	Gradient descent converges faster
Logistic Regression	✅ Often	Better optimization
Neural Networks	✅ Yes	Speeds up training
Decision Trees, Random Forest	❌ No	Not affected by scale
🔷 Summary
Term	Meaning
Normalization	Scaling values between 0 and 1
Standardization	Scaling values to have mean 0 and std dev 1
When Needed	When ML model is sensitive to input scale
Goal	Equal weight for all features
✅ In Simple Words:

    Just like you can't compare height in cm and weight in kg directly, machine learning models can’t compare features on different scales.
    Normalization puts everything on the same scale, making it fair and easy for the model to learn patterns.