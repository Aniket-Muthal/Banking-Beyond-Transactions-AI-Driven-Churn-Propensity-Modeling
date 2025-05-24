# Banking-Beyond-Transactions-AI-Driven-Churn-Propensity-Modeling

**Problem Statement:**
- Customer churn is a significant issue for banks, impacting revenue and customer lifetime value. The goal is to develop a machine learning model that predicts whether a customer will churn (leave the bank) based on their demographic, financial, and account activity data.

**Objective:**
- Build a predictive model to classify customers as likely to churn (Exited = 1) or stay (Exited = 0).
- Identify key factors influencing customer attrition.
- Provide actionable insights for customer retention strategies.

**Strategy**
- It is a Supervised Binary Classification problem.
- Along with correctly classifying customers as churn or retain, our focus is to minimize the error of missing customers who are likely to churn as it directly related to revenue of banks.
- To be precise, high recall for positive instances is the requirement.

**Data Dictionary:**

The dataset consists of 10,000 records with 13 features:

1. CustomerId: Unique identifier for each customer.
2. Lastname: Customer's last name (not useful for prediction).
3. CreditScore: Customer's credit rating.
4. Geography: Country of the customer (France, Spain, Germany).
5. Gender: Male or Female.
6. Age: Customer's age.
7. Tenure: Number of years the customer has been with the bank.
8. Balance: Account balance.
9. NumOfProducts: Number of products the customer has with the bank.
10. HasCrCard: Whether the customer has a credit card (1 = Yes, 0 = No).
11. IsActiveMember: Whether the customer is an active member (1 = Yes, 0 = No).
12. EstimatedSalary: Customer's estimated salary.
13. Exited: Target variable (1 = Churned, 0 = Stayed).

**Performance Metrics Summary:**

**1. Accuracy:**

- The model is able to correctly classify 86.7% datapoints of the training data and 85.8% of the unseen test data showcasing good generalization.

**2. Precision:**

a. Class 0 (Retained Customers): **0.93**
- 93% of the predicted retained customers are actually retained.

b. Class 1 (Churned Customers): **0.63**
- 63% of the predicted churned customers actually churned.

**3. Recall:**

a. Class 0 (Retained Customers): **0.89**
- 89% of the retained customers are correctly identified.

b. Class 1 (Churned Customers): **0.75**
- 75% of the churned customers are correctly identified.

**4. F1:**

a. Class 0 (Retained Customers): **0.91**
- The model is correctly identifying 91% of the retained customers with high Precision and Recall.

b. Class 1 (Churned Customers): **0.68**
- The model correctly identifies 68% of the churned instances and misses the other due to imbalanced distribution of churned instances.

**5. Macro Avg:**

- Describes average performance of both the churned and retained classes assigning equal weightage to each class.
- Precision (**0.78**), Recall (**0.82**) and F1 (**0.80**)

**6. Weighted Avg:**

- Describes weighted average performance of both the churned and retained classes by taking into account the distribution of classes.
- Precision (**0.87**), Recall (**0.86**) and F1 (**0.86**)

**Recommendations**
**A. Strategies for impactful features**

**Insights:**

- Age: Older customers are more likely to churn
- Geography: Customers from a low customer base country (Germany) are more likely to churn
- Gender: Feamle customers tend to leave banks at higher rate
- Active Member/ Credit Card: Inactive customers or those with no Credit Cards churn more
- Number of Products: Though less in number, customers with 3 or 4 products churn at higher rate
- Balance: Customers maintaining high balance are churned in high numbers

Any combination of the above features increases the chances of churning.

**Suggestions:**

- Bank may focus on personalized engagement for older customers by offering retirement plans and investment plans.
- Providing door step financial services to senior citizens and proper timely feedback mechanism can enhance customer relationship.
- Bank must prioritize improving services even at the location with small customer base and plan special loyalty programs and perks to retain customers in the region of higher churn rates.
- Gender specific programs to be initiated to enhance banking experiences for female customers like - literacy programs, investment schemes tailored to women.
- Re-engagement campaigns to be launched to re-activate the customers by offering attractive services including digital marketing and banking.
- Engage customers by offering them Credit Cards with perks and competitive rates.
- Bank must also check on the products as to why customers churned even with higher products usage and try to mitigate the issue by offering strong customer support.
- Customers who exited with high balances in the account must be analyzed further to get more insights.

**B. Strategies for less important features**

- Credit Scores, Estimated Salary and Tenure showed minimal impact on the churn.
- Bank must analyze the behavior of these features and try to study their interactions with other features to improve the predictive power.

In general, alongwith re-connect campaigns, Bank must opt for Customer Retention programs which are demographic specific (age, gender and region). That is, try segementing customers in order to offer services and products as per their needs.

**Conclusion**
- A Machine Learning model is built for Bank Churn prediction using Random Forest Classifier.
- I have analyzed various demographic factors like Age, Gender, Country and financial factors like Credit Score, Salary, Balance, Credit Card, Number of Products, Tenure and studied its effect on the likelihood of churn.
- As per the dataset, key factors that influence churn are Age, Products with Bank, possession of Credit Card, Balance, Country and the Gender of the customer.
- The overall performance of the model is well.

**Summary:**

- Good generalization with a high Accuracy of 86% on the chunk of unseen test data and about 84% on the overall unseen test data.
- Good Recall for Churners (75%) indicating that the churned customers are identified well enough while balancing the Precision score.
- AUC-ROC score of 0.8828 suggests models ability to effectively differentiate between churned customers and the retained customers.
- PR-AUC of 0.7189 showcases the moderate balance between Precision and the Recall while capturing the cases of Churned customers.

Using the models predictive power, Bank can proactively identify customers that are at the risk of leaving, enabling it to prioritize strategies for customer retention and thereby maximizing the revenue.
