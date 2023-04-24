# Bank-customer-churn-analysis-and-machine-learning
This is a personal project for practicing. Dataset is available from Kaggle  https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers

## 1. Background
Banks are categorically known for being long-standing business. Customers who stay with a bank for longer periods of time would make the bank more profitable. Therefore understanding and preventing **_customer churn_** is essential of banking success.

Customer churn refers to the percentage of customers who have stopped services provided by a bank or other financial institution. The average bank or financial instutution loses 25-30 percent of its customers every year. When customers churn, they leave behind fewer deposits and fewer opportunities for loans. The lost revenue could have been used to fund new services, hire more staff, etc.. Instead, competitors who pick up those churned customers could use their revenue boost to increase their competitive edge. This is significant drain on resources, so it's important for banks to understand why customers leave and how to prevent this.

## 2. Objectives
- What factors contribute to customer churn?
- Customer churn prediction with machine learning

## 3. Benefits of the analysis
- Try to improve customer experience
- Optimize bank products and services
- Customer retention and revenue generation

## 4. Dataset

Bank customer churn prediction is fundamentally a classification problem, with target variable being categorical (churn vs. no churn).
High level analysis (churn rate) is numerical.

**Dataset**

Dataset used including a total of 14 columns, 10000 entries:

- **RowNumber**—row number only
- **CustomerId**-unique ID
- **Surname**—the surname of a customer
- **CreditScore**—credit score
- **Geography**—a customer’s location
- **Gender**
- **Age**
- **Tenure**— the number of years that the customer has been a client of the bank
- **Balance**
- **NumOfProducts**—the number of products that a customer has purchased through the bank.
- **HasCrCard**—whether or not a customer has a credit card
- **IsActiveMember**
- **EstimatedSalary**—estimate salary
- **Exited**—target, whether or not the customer left the bank, '0' means customer stayed, '1' means customer churned

https://www.kaggle.com/datasets/mathchi/churn-for-bank-customers

- Data processing

>- Data loading/reading
>- Data cleaning
>- Check and process missing values
>- Study feature value information

- Exploratory data analysis and visualisation

>- Check customer churn rate
>- Feature information check and analysis
>- Feature colleration analysis

- Data handling for ML

>- Synthetic minority over-sampling technigues(SMOTE)
>- Data split into train and test sets
>- feature standardization/scalling

- Machine learning (ML) prediction

>- Classifications
>>- Logistic regression
>>- KNeighbours classification
>>- Decision tree classification: split the dataset into smaller subsets, then making decisions based on subsets characteristics
>>- Random forest classification (supervised ML)
>>- Gradient boosting classifier
>>- Support vector machines (SVM): create a hyperplan between two categories

>- ML performance evaluation
>>- Accuracy score: (TP+TN)/(TP+FP+TN+FN)
>>- Precision score: TP/(TP+FP)
>>- Recall score: TP/(TP+FN)
>>- F1 score: accuracy: (2*precision*recall)/(precision+recall)

- Save the model

>- joblib

## Conclusions

- The following factors are likely to affect customer churn:
>- importance of each key factor: Age > Geography > IsActiveMember > Balance > Gender
>>- customers aged around 45 has highest customer churn rate. Generally, for customers aged over 40, a high customer churn rate is espected.
>>- Germany has the highest customer churn rate
>>- Not active member is more likely to stay
>>- Customers with balance around 120,000 has the highest churn rate.
>>- Female customers are more likely to churn

>- Other factors seem to have less impact on customer churn but is still influencing the outcome
>>- Morjority customers own 1-2 products, customers are more likely to churn when they own more then 3 products and no customer has stayed with the Bank for those who owns 4 products.
>>- Morjority clients owns a credit card and customers who have credit card have slighly higher customer churn rate in comparison to those without a card.

- Machine learning predictions carried out indicate that among all clasification modes random forest classifier provides the highest accuracy and precision score of 0.8818 and 0.8475, respectively. 
- The recommended production ML model for prediction customer churn is saved as 'customer_churn_prediction'.
