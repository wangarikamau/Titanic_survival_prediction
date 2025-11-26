# Titanic_survival_prediction
This project applies machine learning techniques to the Kaggle Titanic Survival Prediction Challenge, where the goal is to build a model that predicts whether a passenger survived the Titanic disaster based on features such as age, sex, passenger class, fare, and number of family members onboard.

The project is fully implemented in Python using Pandas for data manipulation and Scikit-learn for modeling.

##  Project Overview


Load train.csv and test.csv

Perform data cleaning and preprocessing

Handle missing values

Encode categorical variables

Train a machine learning model

Generate predictions on the Kaggle test set

Export a submission.csv file with the required format for Kaggle

## Data Preprocessing Steps

The notebook performs several essential cleaning and preprocessing tasks to prepare the data for modeling:

1. Column Removal

The Cabin column was removed due to too many missing values and low predictive value.

2. Handling Missing Values

Missing values were handled carefully to ensure model reliability:

Age values were filled using the median

Fare values (in the test dataset) were filled using the median

Embarked values were cleaned if needed

3. Encoding Categorical Data

Categorical variables were converted into numeric format so they could be used by the model:

Sex was encoded as 0 (male) and 1 (female)

4. Feature Selection

The model was trained using the following features:

Passenger Class (Pclass)

Sex

Age

Number of Siblings/Spouses (SibSp)

Number of Parents/Children (Parch)

Fare

The target variable is Survived.

## Model Training — Logistic Regression

The notebook uses Logistic Regression, a classic and interpretable machine learning model ideal for binary classification problems like survival prediction.

Logistic Regression was chosen because:

It performs well with structured/tabular data

It works effectively with the Titanic dataset

It provides clear probability outputs

It is easy to interpret and fast to train

The model was fitted on the cleaned training data and used to predict survival for the 418 passengers in the test dataset.

## Kaggle Submission File

After training, predictions were generated for the 418 passengers in the test dataset. A submission file was then created containing:

PassengerId

Survived (0 = died, 1 = survived)

## Technologies Used

Python

Pandas

NumPy

Scikit-learn (Logistic Regression)

Google colab