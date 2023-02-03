# Project_Term2_Personal-loan-Modelling_KNN_Naive-Bayes

## Completed project on personal loan modelling post completion term 2

- In this project I have used KNN & Naive Bayes algoritham to costrust a business model

> Problem Statement

USA Leading Bank, provides Multiple products and services to its customers.

Bank having corpus balance and they wanted to scale Personal loan business to boost their Assets base.

Bank is running the campaign to reach out the existing saleried customers with Personal Loan Product offering.

As of now only 9.60% customer have accepted the offer. Response to the campaign is below expectations.

Bank targeting the customers who have already cosuming the Asset product like Credit Cards and Mortgage loans.

Bank is also targeting customers who have not taken any loans but having banking relationship and using othe product like Securities Account & CD Account.

Looking after below par response to the campaign bank wanted to analyse key factors to improve personal loan business and make this campaign successful. 

- Distribution of target variable

![image](https://user-images.githubusercontent.com/106458239/216603714-a928eac4-bfe4-4dc9-872f-a8860bfabe18.png)


> Scores achieved using KNN algoritham(Default Param)

- Train_score 0.9597333333333333
- Test_score0.9256

> Scores achieved using KNN algoritham(n_neighbours=7)

- Train_score 0.9490666666666666
- Test_score0.9208

![Confusion_Matrix](https://user-images.githubusercontent.com/106458239/216598991-d8c4a4a3-4d8f-4a19-9cf6-cf9581159ad0.png)


> Scores achieved using Naive_Bayes algoritham (Default Param)

- Train_score 0.8805
- Test_score0.894

**Model is Underfitting, hence i used Random forest Select from Model for improving the model performance**

- Below are the important feature selected as per their importance

![top feeatures selected ](https://user-images.githubusercontent.com/106458239/216600031-31234719-a077-43c2-9c4c-50cd1df02923.png)

## Model 1

**Top 4 Features selected are 'Income', 'Family', 'CCAvg', 'Education'** > Scores achieved using Naive_Bayes algoritham (4 Features)

- Train_score 0.914
- Test_score0.907

## Model 2

**Top 3 Features selected are 'Income', 'Family', 'CCAvg'** > Scores achieved using Naive_Bayes algoritham (3 Features)

- Train_score 0.9
- Test_score 0.8808

> Model performance has improved post using top 4 & 3 featues selcted form the Select from Model 

> Train_classification_report= classification_report(y_train, y_train_pred)
>
                 precision    recall  f1-score   support

           0       0.96      0.93      0.94      3399
           1       0.47      0.59      0.52       351

    accuracy                           0.90      3750
   macro avg       0.71      0.76      0.73      3750
weighted avg       0.91      0.90      0.90      3750


> Test_classification_report= classification_report(y_test, y_test_pred)

                precision    recall  f1-score   support

           0       0.94      0.92      0.93      1121
           1       0.43      0.50      0.47       129

    accuracy                           0.88      1250
   macro avg       0.69      0.71      0.70      1250
weighted avg       0.89      0.88      0.88      1250

![Confusion_Matrix](https://user-images.githubusercontent.com/106458239/216602300-cd6f475b-90b1-475a-b173-2263e1264759.png)


## Model predicted 3168 instances correctly for negative class while 207 instances were predicted correctly for positive class. Model identified 144 instance negative but in actual they were positive. Model identified 231 instances positive but in actual they were negative.

## Test Data: Model predicted 1036 instances correctly for negative class while 65 instances were predicted correctly for positive class. Model identified 85 instances negative but in actual they were positive. Model identified 64 instances positive but in actual they were negative.
