# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm

1.Import the libraries and read the data frame using pandas.

2.Calculate the null values present in the dataset and apply label encoder.

3.Determine test and training data set and apply decison tree regression in dataset.

4.Calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: S.Renuga
RegisterNumber:212222230118

import pandas as pd
data=pd.read_csv("/content/Salary.csv")

data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()

x=data[["Position","Level"]]
y=data["Salary"]

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)


from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_pred)
mse

r2=metrics.r2_score(y_test,y_pred)
r2

dt.predict([[5,6]])
  
*/
```

## Output:

## data.head()
![Screenshot 2023-10-12 210742](https://github.com/RENUGASARAVANAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119292258/351717be-0284-40cb-bdfa-357258f04ddd)

## data.info()

![Screenshot 2023-10-12 210821](https://github.com/RENUGASARAVANAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119292258/c4e3ee02-f089-4c48-a31d-2be75b176729)

## isnull() and sum()

![Screenshot 2023-10-12 210918](https://github.com/RENUGASARAVANAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119292258/6a54042a-ad93-4813-81aa-4479e8ce5d5e)

## data.head() for salary

![Screenshot 2023-10-12 211036](https://github.com/RENUGASARAVANAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119292258/dbcc8998-eeac-4244-b60b-20694f1779c1)

## MSE value

![Screenshot 2023-10-12 211127](https://github.com/RENUGASARAVANAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119292258/12cd27fe-9b43-45f6-bd41-9eae538bba4a)

## r2 value

![Screenshot 2023-10-12 211203](https://github.com/RENUGASARAVANAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119292258/dcedca1a-0fd2-4ad6-8beb-4a2b1223f570)

## data prediction

![Screenshot 2023-10-12 211313](https://github.com/RENUGASARAVANAN/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119292258/99fd8761-3ddd-4c5a-b0ec-887fc3bddbca)



## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
