# 📊 Telecomm Customer Churn Prediction & Business Impact Analysis

## 🎯 Project Overview
Customer churn is one of the most significant challenges in the telecommunications industry. This project aims to build a predictive machine learning model to identify at-risk customers and understand the underlying drivers of churn. 

Unlike standard academic projects that focus solely on accuracy, this project prioritizes **Recall**, ensuring that the business identifies as many potential churners as possible (80%) to maximize the effectiveness of retention strategies.

## 🚀 Key Business Findings
* **Revenue at Risk:** High-paying customers with high `MonthlyCharges` are more likely to leave.
* **The "New Customer" Vulnerability:** Tenure is a critical predictor; the majority of churn occurs within the first 6 months of a contract.
* **Contractual Influence:** Customers on **Month-to-month** contracts have a significantly higher churn rate compared to those on 1 or 2-year commitments.
* **Retention Value:** By implementing the final model, the business can potentially retain **$7,830 in net revenue** per 1,400 customers evaluated.

## 🛠️ Technical Workflow

### 1. Data Cleaning & Preprocessing
* Converted `TotalCharges` to numeric and handled missing values.
* Performed feature encoding (**One-Hot** and **Binary**) to prepare categorical data for modeling.
* Standardized numerical features using `StandardScaler`.

### 2. Handling Class Imbalance (SMOTE)
The dataset was naturally imbalanced (approx. 26% churners). We implemented **SMOTE (Synthetic Minority Over-sampling Technique)** on the training set, which successfully boosted the model's **Recall for churners from 0.47 to 0.80**.

### 3. Model Benchmarking
We compared three different architectures to find the best balance between predictive power and interpretability:
* **Logistic Regression (Winning Model):** AUC 0.832 | Recall 0.80
* **Random Forest:** AUC 0.819 | Recall 0.47
* **XGBoost:** AUC 0.812 | Recall 0.54

## 📈 Evaluation Metrics
* **ROC-AUC Score:** 0.83 (Excellent discriminative power).
* **Recall (Sensitivity):** 0.80 (We correctly identify 80% of actual churners).
* **Precision:** 0.50 (Optimized for proactive outreach rather than conservative prediction).

## 🧰 Technologies Used
* **Python** (Pandas, NumPy)
* **Visualization:** Matplotlib, Seaborn
* **Machine Learning:** Scikit-Learn, XGBoost, Imbalanced-Learn (SMOTE)
* **Environment:** Google Colab / Jupyter Notebook

## 💡 Recommendations
1.  **Shift to Long-term Contracts:** Incentivize month-to-month users to switch to 1-year plans.
2.  **Proactive Support:** Target new customers (low tenure) with enhanced onboarding and support.
3.  **Price Sensitivity:** Re-evaluate the value proposition for Fiber Optic customers, as they show higher churn despite the premium service.
