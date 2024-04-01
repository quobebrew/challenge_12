## Overview of the Analysis

The purpose of this analysis is to develop machine learning models and various techniques to train and evaluate models with imbalanced classes to predict credit risk in a lending scenario. The dataset contains historical lending activity imported from a csv file, lending_data.csv, and the goal is to predict the creditworthiness of borrowers based on various financial features like loan size, interest rate, borrower income, debt to income ratio, derogatory marks, total debts, loan status and number of accounts.

The data includes information such as loan status (0 for healthy loans and 1 for high-risk loans) and financial attributes of borrowers.

The main variables I was trying to use Logistic Regression model to predict the loan status, specifically distinguishing between healthy (0) and high-risk (1) loans.

The analysis involved several stages of the machine learning process, including data preprocessing, model training, evaluation, and comparison.

I used the Logistic Regression algorithm as primary model and employed resampling techniques like RandomOverSampler to address class imbalance.

## Results

### Machine Learning Model 1:
- Balanced accuracy score: 95.20%
- Precision score:
   Healthy loans (0): 100%
   High-risk loans (1): 85%
- Recall score:
  Healthy loans (0): 99%
  High-risk loans (1): 91%

### Machine Learning Model 2:
- Balanced accuracy score (resampled): 99.37%
- Precision score:
  Healthy loans (0): 100%
  High-risk loans (1): 84%
- Recall score:
  Healthy loans (0): 99%
  High-risk loans (1): 99%
  

## Summary

Both models demonstrate strong performance, but there are notable differences between them. Model 2, trained with resampled data, shows higher balanced accuracy, indicating improved overall predictive performance of about 99% accuracy across the board. However, Model 1 displays higher precision and recall for high-risk loans, which are crucial for identifying potential defaults accurately.

* Does performance depend on the problem we are trying to solve? (For example, is it more important to predict the `1`'s, or predict the `0`'s? )
* Yes performance depends on the problem we are trying to solove. In the case of loans, it's crucial to know which loans might not get paid back (the `1`s) and which ones are safe (the `0`s). Sometimes, it's more important to catch the risky loans (`1`s) because if we miss them, it could cost the bank a lot of money. But if we accidentally think a safe loan (`0`) is risky, it's not as bad - we might just miss out on making a loan. So, when we're choosing which model to use, we need to think about what matters most to the bank and pick the one that helps them the most.


