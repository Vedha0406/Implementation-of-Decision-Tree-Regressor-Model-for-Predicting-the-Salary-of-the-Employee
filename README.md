# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.

2.Upload the dataset and check for any null values using .isnull() function.

3.Import LabelEncoder and encode the dataset.

4.Import DecisionTreeRegressor from sklearn and apply the model on the dataset.


5.Predict the values of arrays.

6.Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.

7.Predict the values of array.

8.Apply to new unknown values.
  

## Program:
```
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by:GAYATHRI.K
RegisterNumber:212223230061
 import pandas as pd
 data = pd.read_csv("Salary.csv")
 data.head()
 data.info()
 data.isnull().sum()
 from sklearn.preprocessing import LabelEncoder
 le = LabelEncoder()
 data["Position"] = le.fit_transform(data["Position"])
 data.head()
 x = data[["Position", "Level"]]
 y = data["Salary"]
 from sklearn.model_selection import train_test_split
 x_train, x_test, y_train, y_test = train_test_split(x, y, test_size=0.2)
 from sklearn.tree import DecisionTreeRegressor
 dt = DecisionTreeRegressor()
 dt.fit(x_train, y_train)
 y_pred = df.predict(x_test)
 from sklearn import metrics
 mse = metrics.mean_squared_error(y_test, y_pred)
mse
 r2 = metrics.r2_score(y_test, y_pred)
 r2
 dt.predict([[5,6]])
````
## OUTPUT
![image](https://github.com/user-attachments/assets/120f02f7-ab84-4ca4-b5e7-6e270256d7a7)
![image](https://github.com/user-attachments/assets/d21d98d4-1e10-4a41-aec4-fd95f6e968cc) ![image](https://github.com/user-attachments/assets/5dd65ad7-c531-42eb-80bb-13829038ee18)




## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
