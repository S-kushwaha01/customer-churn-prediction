# Customer Churn Prediction using Machine Learning

## 📌Project Overview
Customer churn refers to customers who stop using a company’s service.  
In this project, we build a machine learning model to predict customer churn using historical customer data from a telecom company.

The goal is to identify customers who are likely to leave, so businesses can take preventive actions such as discounts, better support, or personalized offers.

## 🎯 Problem Statement
Telecom companies lose revenue when customers churn.  
This project aims to:  
- Analyze customer behavior
- Identify factors contributing to churn
- Build ML models to predict churn accurately

 
## 📂 Dataset Description
Dataset: IBM Telco Customer Churn Dataset   
- Total Records: 7,043 customers  
- Total Features: 21  
- Target Variable: Churn (Yes = customer left, No = customer stayed)  

Key Features:  
- `tenure` – Number of months customer stayed  
- `MonthlyCharges` – Monthly bill amount  
- `TotalCharges` – Total amount charged  
- `Contract` – Contract type  
- `PaymentMethod` – Payment method  
- `InternetService` – Internet service type

## 🔍 Exploratory Data Analysis (EDA) – Key Insights
- Dataset is **imbalanced**, reflecting real-world customer behavior
- Customers with low `tenure` are more likely to churn
- Higher `MonthlyCharges` increase churn risk
- `Month-to-month` contracts have the highest churn rate
- Customers using `Electronic check` payment method churn more
- `Long-term contracts` significantly reduce churn


## ⚙️ Data Preprocessing & Feature Engineering
- Converted `TotalCharges` to numeric format
- Handled missing values using **median imputation**
- Encoded categorical variables using **One-Hot Encoding**
- Split data into training and testing sets (**80/20**)
- Applied **feature scaling** where required

---

## ⚖️ Class Imbalance Handling
Instead of using a single global resampling method, class imbalance was handled **individually for each model** using model-specific techniques, such as:
- `Class weight` adjustment
- `Decision threshold` tuning
- `Model-internal` imbalance handling

This approach resulted in **better and more stable performance** compared to applying **SMOTE globally**.


## 🤖 Machine Learning Models Used
- `Logistic Regression` – Baseline model
- `Support Vector Machine (SVM)`
- `XGBoost Classifier`

---

## 📊 Evaluation Metrics
- `Accuracy`
- `Precision`
- `Recall` *(primary metric)*
- `F1 Score`


