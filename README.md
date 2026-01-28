# EX.NO.01   Introduction to Kaggle and Data preprocessing
## NAME: PRIYADHARSHINI P
## REGISTER NO: 212224040252
## DATE: 27-01-2026
## EX.NO.01   Introduction to Kaggle and Data preprocessing</H1>

## AIM:

To perform Data preprocessing in a data set downloaded from Kaggle

## EQUIPMENTS REQUIRED:
Hardware – PCs
Anaconda – Python 3.7 Installation / Google Colab /Jupiter Notebook

## RELATED THEORETICAL CONCEPT:

**Kaggle :**
Kaggle, a subsidiary of Google LLC, is an online community of data scientists and machine learning practitioners. Kaggle allows users to find and publish data sets, explore and build models in a web-based data-science environment, work with other data scientists and machine learning engineers, and enter competitions to solve data science challenges.

**Data Preprocessing:**

Pre-processing refers to the transformations applied to our data before feeding it to the algorithm. Data Preprocessing is a technique that is used to convert the raw data into a clean data set. In other words, whenever the data is gathered from different sources it is collected in raw format which is not feasible for the analysis.
Data Preprocessing is the process of making data suitable for use while training a machine learning model. The dataset initially provided for training might not be in a ready-to-use state, for e.g. it might not be formatted properly, or may contain missing or null values.Solving all these problems using various methods is called Data Preprocessing, using a properly processed dataset while training will not only make life easier for you but also increase the efficiency and accuracy of your model.

**Need of Data Preprocessing :**

For achieving better results from the applied model in Machine Learning projects the format of the data has to be in a proper manner. Some specified Machine Learning model needs information in a specified format, for example, Random Forest algorithm does not support null values, therefore to execute random forest algorithm null values have to be managed from the original raw data set.
Another aspect is that the data set should be formatted in such a way that more than one Machine Learning and Deep Learning algorithm are executed in one data set, and best out of them is chosen.


## ALGORITHM:
STEP 1:Importing the libraries<BR>
STEP 2:Importing the dataset<BR>
STEP 3:Taking care of missing data<BR>
STEP 4:Encoding categorical data<BR>
STEP 5:Normalizing the data<BR>
STEP 6:Splitting the data into test and train<BR>

##  PROGRAM:
```
import pandas as pd
import io
from sklearn.preprocessing import StandardScaler
from sklearn.preprocessing import MinMaxScaler
from sklearn.model_selection import train_test_split

df = pd.read_csv("Churn_Modelling.csv")
df

df.isnull().sum()

df.fillna(0)
df.isnull().sum()

df.duplicated()

df['EstimatedSalary'].describe()

scaler = StandardScaler()
inc_cols = ['CreditScore', 'Tenure', 'Balance', 'EstimatedSalary']
scaled_values = scaler.fit_transform(df[inc_cols])
df[inc_cols] = pd.DataFrame(scaled_values, columns = inc_cols, index = df.index)
df

x = df.iloc[:, :-1]
y = df.iloc[:, -1]

print("X Values")
x

print("Y Values")
y

x_train, x_test, y_train, y_test = train_test_split(x, y, test_size = 0.2, random_state = 42)

print("X Training data")
x_train

print("X Testing data")
x_test

print("Lenght of X_test ",len(X_test))
```

## OUTPUT:
# Read the dataset :
<img width="1609" height="522" alt="image" src="https://github.com/user-attachments/assets/c4bcb8cb-9a3c-4ba8-828f-dde2d87e5bf4" />



# Finding the missing values:
<img width="262" height="628" alt="image" src="https://github.com/user-attachments/assets/5eabd76e-0d5c-4775-9745-4cac9263d222" />



# Handling missing values:
<img width="1618" height="546" alt="image" src="https://github.com/user-attachments/assets/5283d989-1724-42e4-ac93-c6cd8e5c97aa" />



# Check for duplicates:
<img width="245" height="570" alt="image" src="https://github.com/user-attachments/assets/80a9c75f-faee-434d-9e90-4dfac7fa6ade" />


# Detect outliers:
<img width="340" height="424" alt="image" src="https://github.com/user-attachments/assets/e9be3e3e-a089-4a09-a9e5-f312666c312d" />


# Normalize the dataset:
<img width="1631" height="518" alt="image" src="https://github.com/user-attachments/assets/099a41eb-38c7-4084-84bf-9d10919e8586" />


# Split the dataset into input and output:

<img width="1550" height="547" alt="image" src="https://github.com/user-attachments/assets/ffbf00e2-b2e3-4923-9d89-bcddcdecd007" />

<img width="281" height="605" alt="image" src="https://github.com/user-attachments/assets/d5f2741e-ec83-4559-a3c5-cb4bde4c196c" />


# Print the training data and testing data:
<img width="1585" height="545" alt="image" src="https://github.com/user-attachments/assets/36ac50b8-ee98-4cdc-b0b9-fc734ef9e5d3" />

<img width="335" height="56" alt="image" src="https://github.com/user-attachments/assets/dba8dd72-84c1-4ee9-bdc6-7e7aea6f6d26" />

<img width="1538" height="555" alt="image" src="https://github.com/user-attachments/assets/1a774957-a17f-457c-9854-e9b5428e1f6d" />



## RESULT:
Thus, Implementation of Data Preprocessing is done in python  using a data set downloaded from Kaggle.


