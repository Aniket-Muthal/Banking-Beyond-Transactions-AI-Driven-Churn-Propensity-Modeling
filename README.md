# 🏦 Banking Beyond Transactions: AI-Driven Churn Propensity Modeling

This project aims to **predict customer churn** for a retail bank using demographic, behavioral, and account-level data. By identifying at-risk customers early, the bank can **proactively intervene**, improve retention, and protect long-term revenue.

---

## 📌 Problem Statement

Customer churn is a critical concern for banks. Losing a valuable customer not only affects immediate revenue but also impacts lifetime customer value. Traditional churn management is often reactive. This project aims to shift the paradigm toward **predictive, data-driven retention strategies**.

---

## 🎯 Objectives

- ✅ Build a machine learning model to classify customers as **likely to churn (Exited=1)** or **retain (Exited=0)**
- ✅ Understand key demographic and behavioral drivers of churn
- ✅ Provide **actionable recommendations** to improve customer retention
- ✅ Focus on **high recall** for churners to minimize missed exits

---

## 🧾 Dataset Overview

The dataset includes **10,000 customer records** and 13 features:

| Feature         | Description                                       |
|------------------|---------------------------------------------------|
| CustomerId       | Unique customer identifier (non-predictive)       |
| Lastname         | Surname of customer (non-predictive)              |
| CreditScore      | Customer’s credit rating                          |
| Geography        | Country of the customer (France, Spain, Germany)  |
| Gender           | Male or Female                                    |
| Age              | Customer age                                      |
| Tenure           | Years the customer has been with the bank         |
| Balance          | Account balance                                   |
| NumOfProducts    | # of bank products used                           |
| HasCrCard        | 1 = Yes, 0 = No                                    |
| IsActiveMember   | 1 = Yes, 0 = No                                    |
| EstimatedSalary  | Estimated salary                                  |
| Exited (Target)  | 1 = Churned, 0 = Stayed                           |

---

## 🛠️ Strategy

- 📊 **Problem Type**: Supervised Binary Classification  
- 🚨 **Business Priority**: Reduce False Negatives - missing churners hurts revenue  
- 📌 **Modeling Goal**: Maximize **Recall** for Exited = 1 while maintaining fair Precision  

---

## 📈 Model Performance

| Metric            | Class 0 (Retained) | Class 1 (Churned) |
|-------------------|--------------------|--------------------|
| Precision         | 0.93               | 0.63               |
| Recall            | 0.89               | 0.75               |
| F1 Score          | 0.91               | 0.68               |

### Global Metrics

| Metric       | Value  |
|--------------|--------|
| Accuracy     | 86%    |
| ROC-AUC      | 0.88   |
| PR-AUC       | 0.72   |
| Macro F1     | 0.80   |
| Weighted F1  | 0.86   |

> 📌 **Interpretation**: The model performs well on both classes, especially achieving high **recall on churners** (75%), which aligns with business strategy.

---

## 🧠 Key Insights

- 📌 **Age**: Older customers are more likely to churn  
- 🌍 **Geography**: Customers from Germany show higher churn  
- ♀️ **Gender**: Female customers churn at higher rates  
- 💤 **Activity**: Inactive members are highly likely to churn  
- 💳 **Credit Card**: Those without a credit card churn more  
- 📦 **NumOfProducts**: Customers with 3–4 products churn more than those with 1–2  
- 💰 **Balance**: High-balance customers churn in greater absolute numbers

---

## 💡 Strategic Recommendations

### A. For High-Impact Features

| Feature          | Recommendation                                                                 |
|------------------|---------------------------------------------------------------------------------|
| Age              | Offer retirement planning and personal engagement for senior citizens          |
| Geography        | Launch loyalty perks in smaller markets like Germany                           |
| Gender           | Design women-centric financial literacy & engagement programs                  |
| Activity         | Run re-engagement campaigns and satisfaction surveys for inactive members      |
| Credit Card      | Promote credit card offerings with exclusive benefits                          |
| Balance          | Investigate reasons for churn among high-balance customers                     |
| NumOfProducts    | Improve support for high-product customers; identify dissatisfaction factors    |

### B. For Low-Impact Features

| Feature            | Action                                                                 |
|--------------------|------------------------------------------------------------------------|
| CreditScore        | Analyze interactions with geography and product usage                  |
| EstimatedSalary    | Consider outlier handling and clustering                              |
| Tenure             | Study effect of tenure in conjunction with age and activity status     |

---

## 📦 Model Pipeline

- 📌 **Data Cleaning**: Remove ID/Name columns, handle outliers
- 📌 **Feature Encoding**: Geography & Gender — One-Hot or Ordinal
- 📌 **Class Rebalancing**: SMOTE / Class weighting
- 📌 **Model**: Random Forest Classifier (ensemble for robustness)
- 📌 **Evaluation**: Detailed metrics on both classes + ROC and PR curves
- 📌 **Explainability**: Feature importance via SHAP or permutation methods

---

## ✅ Final Verdict

The project successfully delivers:

- 📈 **A recall-optimized churn prediction model**
- 🧩 **Comprehensive feature analysis** for targeted intervention
- 🎯 **Strategic segmentation** of customer base
- 💬 **Clear business recommendations** to increase retention

Using this model, the bank can proactively **identify at-risk customers**, deploy personalized engagement, and **maximize revenue per user** across demographics.

---

## 📬 Contact

Project Owner: **Aniket**  
Let’s transform customer insight into strategy 💡📊
- 📧 Email: [aniketmuthal4@gmail.com]
- 🔗 LinkedIn: [https://www.linkedin.com/in/aniket-muthal]
