## Telco Customer Churn

### Problem

Predict behavior to retain customers. You can analyze all relevant customer data
and develop focused customer retention programs.

### Dataset

In the dataset, each row represents a customer, each column contains customer’s
attributes described on the column Metadata.

The data set includes information about:

- Customers who left within the last month – the column is called Churn

- Services that each customer has signed up for :

  - phone,

  - multiple lines,

  - Internet,

  - online security,

  - online backup,

  - device protection,

  - tech support, and

  - streaming TV and movies

- Customer account information – how long they’ve been a customer, contract,
  payment method, paperless billing, monthly charges, and total charges

- Demographic info about customers – gender, age range, and if they have
  partners and dependents

## Project Instructions

### Preprocessing

- Perform initial data preparation by converting the 'TotalCharges' column to
  numeric values and filling missing values with 0.
- Convert the 'Churn' column to binary values, where 'No' is mapped to 0 and
  'Yes' is mapped to 1.- - Split the data into an 80-20 train-test split with a
  random state of “1”. Select these features:  
  categorical = ['gender', 'SeniorCitizen', 'Partner', 'Dependents',
  'PhoneService', 'MultipleLines', 'InternetService','OnlineSecurity',
  'OnlineBackup', 'DeviceProtection', 'TechSupport', 'StreamingTV',
  'StreamingMovies','Contract', 'PaperlessBilling', 'PaymentMethod'] numerical =
  ['tenure', 'MonthlyCharges', 'TotalCharges']

### Feature engineering

- The numerical features should be scaled using StandardScaler, convert the
  output back to a dataframe and put back the column names.
- The categorical features are one-hot encoded using OneHotEncoder(set
  sparse_output to false), convert the output back to a dataframe and put back
  the column names.
- Combine scaled numerical and one-hot encoded categorical features into train
  and test set dataframes (use pd.concat)
- Use scikit learn to train a random forest and extra trees classifier, and use
  xgboost and lightgbm to train an extreme boosting model and a light gradient
  boosting model. Use random_state = 1 for training all models and evaluate on
  the test set. Answer the following questions:

## Resource

- [Kaggle](https://www.kaggle.com/datasets/blastchar/telco-customer-churn/data)

- [IBM -Telco dataset](https://community.ibm.com/community/user/businessanalytics/blogs/steven-macko/2019/07/11/telco-customer-churn-1113)
