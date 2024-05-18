![image](https://github.com/vineeth-pydi/Banking-Customer-Churn/assets/124265210/2cb13bc8-76a7-4447-b8e2-7ced2dc88cf1)

## Understanding Customer Attrition in Banking:

Customer attrition, also known as churn, refers to the phenomenon where customers cease their business relationship with a brand, leading to the termination of their status as paying clients. This is quantitatively represented by the customer churn rate, which is the proportion of customers who discontinue the use of a company's products or services over a given timeframe. Often, it only takes a single negative experience—or a series of them—for a customer to decide to leave. A significant exodus of dissatisfied customers within a certain period can result in substantial financial losses and tarnish the company's reputation.

## Objective for XYZ BANK:

XYZ BANK aims to mitigate this issue by developing a predictive model. This model will utilize various machine learning techniques to accurately forecast the likelihood of customer churn. The goal is to enable the bank to implement preemptive measures, thus minimizing customer attrition and its associated adverse effects.

### Dataset Description and Data Dictionary Overview

Our dataset is designed to support the development of a predictive model for customer churn, specifically for a banking context. It comprises 10,000 entries, each corresponding to a different customer, and is structured across 14 distinct columns, including the target variable **Exited**.

#### Data Dictionary

Below is a summary of each column in the dataset, providing insights into the nature of the data and its relevance to the churn prediction model:

1. **CustomerID**: A unique identifier for each customer. This is likely a nominal variable that does not directly influence the churn prediction but is essential for data management.

2. **Surname**: The last name of the customer. Like the CustomerID, this column is more for identification purposes and is not expected to contribute to the churn prediction model.

3. **CreditScore**: A numerical score assigned to a customer based on their creditworthiness. Higher scores may indicate a lower risk of churn, as they reflect financial stability.

4. **Geography**: The customer's country or region. Geographic location can influence churn due to factors like local competition and economic conditions.

5. **City_Geography**: The classification of the customer's city into categories A, B, or C. 

6. **Gender**: The gender of the customer. Gender might influence the usage patterns of banking products and services, potentially affecting churn rates.

7. **Age**: The age of the customer. Age can be a significant factor in churn, as customer needs and banking behaviors change over life stages.

8. **Tenure**: The number of years the customer has been with the bank. Longer tenure may indicate higher loyalty and possibly a lower propensity to churn.

9. **Balance**: The current balance in the customer's account. The account balance might influence churn, as customers with higher balances may have a stronger relationship with the bank.

10. **NumOfProducts**: The number of products the customer has with the bank. Utilization of multiple products might reduce the likelihood of churn by increasing customer engagement.

11. **HasCrCard**: Indicates whether the customer has a credit card issued by the bank (1 = Yes, 0 = No). Having a credit card could affect customer retention.

12. **IsActiveMember**: Indicates whether the customer is considered an active member (1 = Active, 0 = Inactive). Active customers are likely more engaged and may have a lower churn rate.

13. **EstimatedSalary**: The estimated salary of the customer. Salary levels can influence the choice of banking services and loyalty.

14. **Exited**: The target variable, indicating whether the customer has left the bank (1 = Yes, 0 = No). This is the primary variable of interest for predicting churn.

Understanding the intricacies of these variables will be crucial in designing effective feature engineering strategies and building a robust predictive model.

### Data Dictionary

| **Variable**        | **Definition**                                              |
|---------------------|-------------------------------------------------------------|
| RowNumber           | A unique identifier for each row in the dataset.            |
| CustomerId          | A unique identifier assigned to each customer.              |
| Surname             | The surname of the customer.                                |
| CreditScore         | A measure of the customer's creditworthiness.               |
| Geography           | The customer's geographical location.                       |
| City_Category       | The classification of the customer's city into categories A, B, or C. |
| Gender              | The gender of the customer (e.g., Male, Female).            |
| Age                 | The age of the customer.                                    |
| Tenure              | The duration (in years) the customer has been with the bank.|
| Balance             | The current balance in the customer's account.              |
| NumOfProducts       | The number of banking products the customer uses.           |
| HasCrCard           | Indicates whether the customer has a bank-issued credit card (1 = Yes, 0 = No). |
| IsActiveMember      | Indicates whether the customer is an active member (1 = Active, 0 = Inactive). |
| EstimatedSalary     | The customer's estimated salary.                            |
| **Exited**          | **Indicates whether the customer has left the bank (1 = Yes, 0 = No) - Target Variable.** |

This comprehensive data dictionary serves as a foundational guide for understanding the dataset's structure and the significance of each variable in the context of predicting customer churn. The presence of variables like `City_Category` enriches the dataset by offering additional dimensions for analysis, potentially uncovering more nuanced insights into customer behavior and preferences.

### Work Flow:

**Developing a Predictive Model for Customer Churn: A Step-by-Step Approach**

To construct a predictive model aimed at forecasting customer churn, the following systematic process will be undertaken:

1. **Data Partitioning:**
   - Divide the dataset into two parts: 70% will be allocated for training the model (Train Set), and the remaining 30% will be used for evaluating its performance (Test Set).

2. **Feature Engineering:**
   - Conduct an in-depth analysis to identify and engineer features that are most indicative of customer churn. This step involves selecting relevant variables, creating new features if necessary, and transforming variables to improve model performance.

3. **Accuracy Assessment:**
   - Determine the model's accuracy on both the Training and Test Sets. This involves comparing the model's predictions with actual outcomes to calculate how often the model is correct.

4. **Evaluating Model Generalization:**
   - Compare the accuracy scores obtained on the Training Set with those on the Test Set to assess the model's ability to generalize to unseen data. This comparison is crucial for identifying potential overfitting issues, where a model performs well on training data but poorly on new, unseen data.
