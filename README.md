# Loan Approval Prediction

## About Project

This is a Machine Learning project for predicting whether a loan application will be approved or not.

I used the Loan Approval dataset and trained different Machine Learning models. After comparing the models, I selected Logistic Regression because it gave the best testing and cross-validation performance.

I also created a simple GUI using Tkinter where we can enter the applicant details and predict the loan status.

## Dataset

The dataset used in this project is `loan_approval.csv`.

It contains information like:

- Gender
- Married
- Dependents
- Education
- Self Employed
- Applicant Income
- Coapplicant Income
- Loan Amount
- Loan Amount Term
- Credit History
- Property Area
- Loan Status

## Data Preprocessing

In this project I performed the following preprocessing steps:

- Removed `Loan_ID`
- Removed rows having missing values in some important columns
- Filled missing values in `Self_Employed` using mode
- Filled missing values in `Credit_History` using mode
- Converted `3+` in Dependents to `3`
- Converted categorical values into numerical values using mapping
- Split the data into training and testing data
- Used StandardScaler with Logistic Regression

## Models Used

I tested the following models:

1. Logistic Regression
2. K-Nearest Neighbors
3. Decision Tree
4. Random Forest
5. Support Vector Classifier
6. Gradient Boosting Classifier

After comparing the results, Logistic Regression performed the best for this dataset.

### Logistic Regression Results

- Training Accuracy: 80.54%
- Testing Accuracy: 81.98%
- Cross Validation Score: 80.30%

## Final Model

I trained the final Logistic Regression model on the complete processed dataset and saved it using Joblib.

Model file:

`Loan_Approval_Prediction_Model.pkl`

## GUI

I created a GUI using Tkinter.

The user needs to enter:

- Gender
- Married
- Dependents
- Education
- Self Employed
- Applicant Income
- Coapplicant Income
- Loan Amount
- Loan Amount Term
- Credit History
- Property Area

After clicking the **Predict** button, the application shows:

- Loan Approved
- Loan Not Approved

The input fields are also cleared after prediction so that another prediction can be made.

## How to Run

First install the required libraries:

```bash
pip install pandas numpy scikit-learn matplotlib seaborn joblib
