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
Instead of applying a single global resampling method, class imbalance was handled **individually for each model** using model-specific techniques, such as:
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


## 📈 Model Comparison Summary

- `Logistic Regression` provided the most **balanced and interpretable** performance, delivering strong `Recall` with stable `Precision` and consistent overall behavior.

- `Support Vector Machine (SVM)` achieved higher `Recall` under aggressive tuning but suffered from reduced `Precision` and lower stability, making it less suitable as the final production model.

- `XGBoost` delivered **competitive performance** with a strong balance between `Recall` and `F1 Score`, positioning it as a robust tree-based alternative aligned with industry practices.

📌 **Recall** was prioritized to minimize missed churn customers, as **false negatives directly impact business revenue**.  
However, final model selection emphasized a **balanced trade-off between recall, precision, and model stability**, rather than optimizing recall alone.


## ✅ Final Model Selection
Based on model performance, stability, and interpretability, **Logistic Regression** was selected as the final balanced model for churn prediction.  

While XGBoost demonstrated competitive performance, Logistic Regression provided a better trade-off between recall, precision, and explainability, making it more suitable for real-world deployment and business decision-making.


## 💼 Business Impact

The final model enables proactive identification of high-risk customers, allowing businesses to:
- Launch targeted retention campaigns
- Reduce revenue loss due to churn
- Improve customer lifetime value
- Optimize marketing and support costs





