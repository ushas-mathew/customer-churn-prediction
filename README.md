# Customer Churn Prediction Using Machine Learning

##  Project Overview

This project focuses on predicting customer churn in the telecommunications industry using machine learning.

The project analyses customer demographic, service, contractual and payment information to identify patterns associated with customer churn. Multiple machine learning algorithms are implemented and compared to determine an effective model for predicting whether a customer is likely to leave the service.

The project also investigates the impact of class imbalance and applies SMOTE to improve the prediction of the minority churn class.

---

##  Problem Statement

Customer churn is a major challenge in the telecommunications industry. When customers terminate their subscriptions or move to competitors, organisations can experience revenue loss and reduced market share.

The aim of this project is to use machine learning techniques to identify customers who are more likely to churn and to determine the factors that are associated with customer churn.

---

##  Project Objectives

The main objectives of this project are:

- Analyse customer data and identify factors associated with churn.
- Perform exploratory data analysis (EDA).
- Preprocess and transform the dataset for machine learning.
- Compare different machine learning classification algorithms.
- Evaluate model performance using accuracy, precision, recall and F1-score.
- Apply hyperparameter tuning to improve model performance.
- Address class imbalance using SMOTE.
- Identify important factors associated with customer churn.
- Determine the most effective machine learning approach for this dataset.

---

##  Dataset

The project uses the **Telco Customer Churn dataset**, commonly referred to as the IBM Watson Telco Customer Churn dataset.

The dataset contains:

- **7,043 customer records**
- **21 attributes**

The features include customer demographics, services, contract information, payment methods and customer tenure.

### Important features

Some of the features include:

- Gender
- Senior Citizen
- Partner
- Dependents
- Tenure
- Phone Service
- Multiple Lines
- Internet Service
- Online Security
- Online Backup
- Device Protection
- Tech Support
- Streaming TV
- Streaming Movies
- Contract
- Paperless Billing
- Payment Method
- Monthly Charges
- Total Charges

### Target Variable

`Churn`

The target identifies whether a customer has churned from the service.

---

##  Exploratory Data Analysis

Exploratory Data Analysis was performed to understand customer characteristics and identify relationships between features and churn.

The analysis included:

- Dataset structure and information
- Descriptive statistics
- Churn distribution
- Demographic analysis
- Service analysis
- Payment method analysis
- Contract analysis
- Numerical feature distributions

### Key EDA Findings

Two features showed particularly strong relationships with customer churn:

**Contract Type**

Customers with month-to-month contracts showed a substantially higher churn rate compared with customers on one-year or two-year contracts.

**Payment Method**

Customers using electronic check payments showed a higher churn rate compared with customers using other payment methods.

These findings suggest that contract structure and payment method may be important factors when developing customer retention strategies.

---

##  Data Preprocessing

The following preprocessing techniques were applied:

- Missing-value handling
- Categorical variable encoding
- Feature selection
- Feature scaling
- Train-test splitting

Categorical variables were transformed into numerical representations using encoding techniques.

The dataset was divided using an **80/20 train-test split**.

---

##  Machine Learning Models

Five classification approaches were implemented and compared:

1. Decision Tree
2. Random Forest
3. Support Vector Machine (SVM)
4. SVM with AdaBoost
5. XGBoost

Hyperparameter tuning was also performed to improve model performance.

---

##  Evaluation Metrics

The models were evaluated using:

- Accuracy
- Precision
- Recall
- F1-score
- Confusion Matrix

These metrics provide a more comprehensive evaluation than accuracy alone, particularly because customer churn datasets can contain class imbalance.

---

##  Model Performance Before SMOTE

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Decision Tree | 0.81 | 0.67 | 0.54 | 0.60 |
| Random Forest | 0.81 | 0.69 | 0.53 | 0.60 |
| SVM | **0.82** | 0.69 | 0.60 | 0.64 |
| AdaBoost | 0.77 | 0.54 | 0.74 | 0.63 |
| XGBoost | 0.79 | 0.64 | 0.51 | 0.57 |

Before applying SMOTE, **SVM achieved the highest accuracy of approximately 82%**.

---

##  Handling Class Imbalance with SMOTE

The dataset contained an imbalance between churned and non-churned customers.

To address this issue, **SMOTE (Synthetic Minority Over-sampling Technique)** was applied to generate synthetic samples for the minority class.

This allowed the models to learn the characteristics of churned customers more effectively.

---

##  Model Performance After SMOTE

| Model | Accuracy | Precision | Recall | F1-Score |
|---|---:|---:|---:|---:|
| Decision Tree | 0.93 | 0.91 | 0.96 | 0.94 |
| Random Forest | **0.96** | 0.95 | 0.97 | 0.96 |
| SVM | 0.92 | 0.91 | 0.94 | 0.92 |
| AdaBoost | 0.91 | 0.99 | 0.93 | 0.91 |
| XGBoost | **0.96** | 0.95 | 0.97 | 0.96 |

After applying SMOTE, **Random Forest and XGBoost achieved the strongest overall performance**, with approximately 96% accuracy and an F1-score of 0.96.

---

##  Key Results

The project demonstrated that:

- SVM performed best on the original imbalanced dataset, achieving approximately 82% accuracy.
- Class imbalance had a significant effect on model performance.
- Applying SMOTE substantially improved the performance of the models.
- Random Forest and XGBoost achieved the strongest overall results after SMOTE.
- Contract type and payment method were important factors associated with customer churn.

---

##  Business Insights

The analysis suggests that telecommunications companies could focus on:

- Encouraging customers to move from month-to-month contracts to longer-term contracts.
- Improving the electronic-check payment experience.
- Identifying high-risk customers using predictive models.
- Developing targeted customer retention strategies.
- Using customer characteristics and service information to identify potential churn risks.

---

##  Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- XGBoost
- Imbalanced-learn
- Jupyter Notebook

---

##  Project Structure

```text
customer-churn-prediction/
│
├── README.md
│
├── data/
│   └── customer_churn.csv
│
├── notebooks/
│   └── customer_churn_prediction.ipynb
│
├── reports/
│   └── final.pdf
│
├── images/
│   ├── churn_distribution.png
│   ├── contract_comparison.png
│   ├── payment_method_comparison.png
│   ├── confusion_matrix.png
│   └── model_comparison.png
