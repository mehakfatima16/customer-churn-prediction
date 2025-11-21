# Customer Churn Prediction — End-to-End Machine Learning Project

A complete churn prediction project built using Python, scikit-learn, and Google Colab.  
This project identifies high-risk customers and provides actionable business insights for improving retention.

##  Project Overview

This project predicts whether a customer is likely to churn based on:
- Billing patterns  
- Contract type  
- Internet/phone service usage  
- Technical support history  
- Monthly/Total charges  
- Customer lifetime value (CLTV)  
- Service quality feedback  

The pipeline includes **data cleaning → feature engineering → EDA → model training → evaluation → exporting high-risk customers**.



## Data Cleaning & Preprocessing

Key steps performed:
- Fixed inconsistent numeric fields (like “Total Charges”).  
- Removed high-cardinality location fields (Country, State, City).  
- Converted Yes/No features to numeric (1/0).  
- Split `"Lat Long"` into separate Latitude and Longitude columns.  
- One-hot encoded all categorical variables.  
- Created the target variable **Churn** using `"Churn Reason"`.  

Final dataset shape: **7043 rows × 36 features**


##  Exploratory Data Analysis (EDA)

Exploration included:
- Churn distribution (74% non-churn, 26% churn).  
- Churn by contract type (month-to-month highest).  
- Monthly charge comparison for churn vs non-churn.  
- Tenure patterns — customers with shorter tenure churn more.

---

##  Machine Learning Models

Two models were trained:

### **1. Logistic Regression**
A linear baseline model for interpretability.

### **2. Random Forest Classifier**
Final chosen model (n_estimators=300).

It produced:
- Accurate probability scores  
- Strong feature importance  
- Better performance than baseline  

---

##  Top 100 At-Risk Customers

The model produces a CSV file listing the **top customers most likely to churn**, sorted by predicted probability.

📄 File included in the repo:  
`outputs/top100_at_risk_customers.csv`

This is extremely useful for:
- Sales teams  
- Retention campaigns  
- CRM integrations  
- Marketing segmentation  

---

##  Key Features Influencing Churn

Top predictors identified by the model:
- Monthly Charges  
- Total Charges  
- Contract Type  
- Tenure Months  
- Internet/Phone Service features  
- Technical Support  
- Payment Method  

These insights directly inform business strategies.


