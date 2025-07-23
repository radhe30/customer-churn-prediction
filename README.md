#Customer Churn Prediction – Model Training & Analysis

This repository contains a complete pipeline to build and evaluate a machine learning model for predicting customer churn using the [Telco Customer Churn dataset](https://www.kaggle.com/datasets/blastchar/telco-customer-churn). 
The goal is to help businesses proactively identify customers who are likely to leave and design retention strategies.

---

##Objective

Customer churn refers to customers discontinuing their subscription or ceasing to use a service. This project leverages historical customer data and machine learning to:

- Understand key factors driving churn.
- Train a predictive model using Random Forest.
- Evaluate model performance.
- Explain model decisions using SHAP values.
- Save the trained model for deployment or further analysis.

##Project Structure
customer_churn_prediction/
├── churn_model/
│ ├── data/
│ │ └── Telco-Customer-Churn.csv # Dataset
│ ├── churn_prediction.py # Main training & analysis script
├── best_random_forest_model.pkl # Saved trained model
├── README.md # Project documentation

---------# Key Components #-----------

#Exploratory Data Analysis (EDA)

Overview of data types and statistics
Class balance visualization
Correlation heatmap of numerical features

#Feature Engineering

New feature: AverageMonthlySpend = MonthlyCharges × tenure
Binned tenure into categories (TenureCategory)

#Preprocessing

Handling missing values and converting datatypes
Encoding categorical variables (binary + one-hot)
Scaling numerical features with StandardScaler

#Modeling

Train-test split (80/20)
Random Forest Classifier used as the baseline model

Model evaluation using:
Classification report (Precision, Recall, F1-Score)
Confusion Matrix visualization

#Model Explainability

SHAP (SHapley Additive exPlanations) is used to visualize feature importance and understand model decisions.

#Model Saving

The trained model is saved as a .pkl file using joblib for later use.

#Sample Output

Classification Report:

markdown
Copy
Edit
precision    recall  f1-score   support
     0          ...       ...      ...
     1          ...       ...      ...
accuracy                             ...
Confusion Matrix: Displayed using Seaborn heatmap

SHAP Summary Plot: Top features driving churn predictions

Dataset Features (Telco Customer Churn)
Customer info: gender, senior citizen status, partner/dependents

Service usage: internet service, online security, tech support

Contract details: tenure, payment method, paperless billing

Target variable: Churn (Yes/No)

Output
Trained model: best_random_forest_model.pkl

Visuals: EDA plots, confusion matrix, SHAP plot (displayed at runtime)

✅ Future Improvements
Add cross-validation and hyperparameter tuning (e.g., GridSearchCV)

Compare performance across multiple models

Deploy via FastAPI or Streamlit interface

Save scaler along with the model for consistent inference

👤 Author
Name: Radha Mohan Choudhary
Email: choudhary0030430@gmail.com
GitHub: github.com/radhe30
