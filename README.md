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
Developed by:VEDHASHREE.G
RegisterNumber:212223240171
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
## Data.Head():
![279486017-17219e1b-9545-45e2-bb45-dd459016cbf9](https://github.com/user-attachments/assets/9aeef499-c8e2-4a33-b9f8-9492e410437d)
## Data.info():
![279486035-6c499887-944a-476d-b365-f406cc541e6f](https://github.com/user-attachments/assets/dece8495-a8c6-4745-b9b3-54ef3a535505)
## isnull() and sum():
![279486050-e97ab81f-f8b9-4813-83de-327da3214afe](https://github.com/user-attachments/assets/c3b34466-c99a-42fb-8202-8c5bd2a3a011)
## Data.Head() for salary:
![279486068-ffc344dd-39b6-4370-9282-468f4642736c](https://github.com/user-attachments/assets/98cd7a18-5e38-447a-8893-cf4b4bc72373)
## MSE Value:
![279486086-d063c559-f82f-4a52-b1fd-74c153c7d36e](https://github.com/user-attachments/assets/a68d0fb0-4a68-4ce0-9043-884bc90e9802)
## r2 Value:
![279486100-2956ebf4-c1b2-4a45-9365-21f67717ebc4](https://github.com/user-attachments/assets/f4204c3e-4db9-4e80-9e81-325f79f15001)
## Data Prediction:
![279486119-516cbe0b-9937-4dd6-a5a8-1ac01a6673eb](https://github.com/user-attachments/assets/6f1f2577-5e56-4c7f-9896-4d150817d61f)
## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
