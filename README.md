# Bank Customer Churn Prediction Using Logistic Regression

## 📌 Domain Explanation

Bank customer churn refers to customers leaving or closing their bank accounts. Retaining existing customers is important because acquiring new customers can be more costly than maintaining existing relationships.

Machine learning can help banks identify customers who are likely to leave by analyzing their demographic, financial, and account-related information.

## 🎯 Problem Statement

The objective is to develop a machine-learning classification model to predict whether a customer will churn from ABC Bank.

Customer information such as credit score, age, geography, balance, tenure, number of products, credit-card ownership, and active membership is analyzed to identify patterns associated with customer churn.

## 📊 Dataset

The dataset contains customer demographic, financial, and account-related information.

| Feature         | Description                                             |
| --------------- | ------------------------------------------------------- |
| Customer ID     | Unique identification number                            |
| Surname         | Customer's surname                                      |
| Credit Score    | Credit score of the customer                            |
| Geography       | Country/location of the customer                        |
| Gender          | Gender of the customer                                  |
| Age             | Age of the customer                                     |
| Tenure          | Number of years with the bank                           |
| Balance         | Customer's account balance                              |
| NumOfProducts   | Number of bank products used                            |
| HasCrCard       | Whether the customer has a credit card                  |
| IsActiveMember  | Whether the customer is an active member                |
| EstimatedSalary | Estimated salary of the customer                        |
| Churn           | Target variable indicating whether the customer churned |

## 🔍 Exploratory Data Analysis

EDA was performed to understand the dataset and identify relevant features. The analysis included:

* Dataset shape and information
* Descriptive statistics
* Missing value checking
* Duplicate value checking
* Age distribution
* Customer churn distribution
* Correlation analysis

### Key EDA Findings

* Most customers are between 25 and 45 years old.
* The majority of customers have not churned.
* The dataset is imbalanced, with non-churned customers significantly higher than churned customers.
* Age has the strongest positive relationship with churn.
* Active membership has a negative relationship with churn.
* Balance has a weak positive relationship with churn.
* Credit score, tenure, and estimated salary have very little correlation with churn.

## 🤖 Model

### Logistic Regression

Since the target variable **Churn** has two possible outcomes, 0 and 1, this is a binary classification problem.

Logistic Regression is used to predict the probability of a customer churning or staying with the bank.

### Data Preprocessing

* Customer ID was removed because it does not contribute to prediction.
* Categorical variables such as gender and geography were converted using one-hot encoding.
* Numerical features were standardized using feature scaling.
* The dataset was divided into **80% training** and **20% testing** data.
* Stratified sampling was used to maintain the proportion of churned and non-churned customers.

## 📈 Model Evaluation

The Logistic Regression model was evaluated using:

* **Accuracy**
* **Precision**
* **Recall**
* **F1-Score**
* **ROC-AUC Score**
* **Confusion Matrix**

Recall is particularly important for customer churn because identifying more potential churners can help the bank take preventive action.

## 💡 Insights

* Older customers are comparatively more likely to churn.
* Active customers are less likely to leave the bank.
* Customer engagement plays an important role in retention.
* The dataset is imbalanced, which should be considered during model evaluation.
* Logistic Regression can provide churn probabilities that help identify customers at higher risk of leaving.

## 🛠️ Technologies Used

* Python
* Google Colab
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn

## 📁 Files

* `Bank_Customer_Churn.ipynb` – Google Colab/Jupyter Notebook
* `Bank_Customer_Churn.csv` – Dataset
* `README.md` – Assignment documentation

## ✅ Result

The Logistic Regression model was successfully developed to predict customer churn for ABC Bank. The analysis identified important factors associated with churn and can help support customer retention strategies.
