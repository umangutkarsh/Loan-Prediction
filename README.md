# Loan-Prediction
Given historical data on loans given out with information on whether or not the borrower defaulted (charge-off), can we build a model that can predict wether or nor a borrower will pay back their loan? This way in the future when we get a new potential customer we can assess whether or not they are likely to pay back the loan.

The dataset used is a subset of the LendingClub DataSet obtained from Kaggle: https://www.kaggle.com/wordsforthewise/lending-club

LendingClub is a US peer-to-peer lending company, headquartered in San Francisco, California. It was the first peer-to-peer lender to register its offerings as securities with the Securities and Exchange Commission (SEC), and to offer loan trading on a secondary market. LendingClub is the world's largest peer-to-peer lending platform.


Introduction: The Problem statement of this project is that LendingClub is a US peer-to-peer lending company, headquartered in San Francisco, California, and it lends loan to it's customers but the problem is that it's customers dosen't repay back the loan, so the main motive is to build a model using Artificial Neural Network(which is a part of Deep Learning), so that we can predict whether or not the borrower will repay back their loan, which will help the company to assess whether or not the customer will repay back their loan on the basis of their data.


Data Analysis libraries are used for data analysis, Exploratory Data Analysis is done to assess properly, about the data given.
A lot of Feature Engineering work is done and dummy variables are also created on the dataset, so as to fill the missing values, and deal with the missing columns.

1. Because of feature engineering, a lot of correlation was found between some coloumns of the datset.
2. Since the dataset was highly imbalanced, the technique of over sampling is also applied to balance the label which we are tryign to predict, as without balancing the accuracy was around 89%, but using the SMOTE using the imblearn library, the accuracy of the model increased to 91%
3. There are other resampling techniques, such as, undersampling could also be done but then a large amount of data might have got lost, and so over-sampling was choosen as the final technique.
4. When training the model, adam optimizer could have been used, but then there was a huge increment in the loss and the accuracy came out to be around 52%, so then Stochastic Gradient Descent technique was applied as the optimizer.
5. SMOTE was applied before train_test_split, it could also have been applied before that since it dosen't create duplicate data.

Conclusion: 
1. F1-Score came out to be 0.90 
2. Accuracy = 91%
3. 1236 data was misclassified (Type1 error and Type2 error)
