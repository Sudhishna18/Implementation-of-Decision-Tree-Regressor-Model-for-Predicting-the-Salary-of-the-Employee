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

4.calculate Mean square error,data prediction and r2.



## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Sudhishna P
RegisterNumber: 212224040336
*/
import pandas as pd
data=pd.read_csv("C:\\Users\\admin\\Downloads\\Salary (1).csv")
data.head()
data.info()
data.isnull().sum()
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x=data[["Position","Level"]]
x.head()
y=data["Salary"]
y.head()
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:

![image](https://github.com/user-attachments/assets/7b1aeecc-f249-46ee-85a4-7e9ea620982c)

![image](https://github.com/user-attachments/assets/897e1cbb-40f5-4c01-95d1-1da0294e4134)

![image](https://github.com/user-attachments/assets/a0af1809-3d46-4cda-bc40-beb911408a70)

![image](https://github.com/user-attachments/assets/61660150-8ec9-4c77-9802-77632b692063)

![image](https://github.com/user-attachments/assets/3daf7366-dfee-4083-91d9-bf217003cc29)

![image](https://github.com/user-attachments/assets/a8cd939e-f2d4-48a8-a141-52db571dc5ae)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
