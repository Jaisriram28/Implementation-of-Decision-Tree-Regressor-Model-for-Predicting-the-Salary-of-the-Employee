Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the libraries and read the data frame using pandas.
2. Calculate the null values present in the dataset and apply label encoder.
3. Determine test and training data set and apply decison tree regression in dataset.
4. calculate Mean square error,data prediction and r2.

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: JAI SRIRAM S
RegisterNumber:  212222040057

import pandas as pd
data=pd.read_csv("/content/Salary.csv")
data.head()

data.info()

data.isnull().sum()

from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data['Position']=le.fit_transform(data['Position'])
data.head()

x=data[['Position','Level']]
y=data['Salary']

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)

from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier()
dt.fit(x_train,y_train)
y_predict=dt.predict(x_test)

from sklearn import metrics
mse=metrics.mean_squared_error(y_test,y_predict)
mse

r2=metrics.r2_score(y_test,y_predict)
r2

dt.predict([[5,6]])

*/
```

## Output:


## Data.Head():


![Screenshot 2024-04-06 113937](https://github.com/Jaisriram28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122092094/a3163e7a-efe0-48af-887a-2ff123abaa19)



## Data.info():

![Screenshot 2024-04-06 113952](https://github.com/Jaisriram28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122092094/0164c53b-24ab-491f-98e0-f9352de0454f)


## isnull() and sum():


![Screenshot 2024-04-06 114022](https://github.com/Jaisriram28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122092094/1aaa1763-e89e-43a2-a935-1a80f66b33af)




## Data.Head() for salary:


![Screenshot 2024-04-06 114042](https://github.com/Jaisriram28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122092094/c09424a4-29f4-4097-8efb-e76c01fa22c7)


## MSE Value:

![Screenshot 2024-04-06 114059](https://github.com/Jaisriram28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122092094/a29a5092-e203-40fa-9e06-b58557dcd332)





## r2 Value:



![Screenshot 2024-04-06 114117](https://github.com/Jaisriram28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122092094/2d8e2f2b-8a51-467e-9e37-4bbb7eb20a3f)


## Data Prediction:
![Screenshot 2024-04-06 114127](https://github.com/Jaisriram28/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/122092094/2f8a1174-c705-493d-811c-256b2089bfcf)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
