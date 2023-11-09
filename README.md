# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the required libraries.
2. Upload the csv file and read the dataset.
3. Check for any null values using the isnull() function.
4. From sklearn.tree inport DecisionTreeRegressor.
5. Import metrics and calculate the Mean squared error.
6. Apply metrics to the dataset, and predict the output 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: Dilip Kumar R
RegisterNumber:212222040037  
*/
import pandas as pd
data=pd.read_csv("/content/Salary(1).csv")
print('data.head():')
data.head()
print('data.info():')
data.info()
print('isnull() and sum():')
data.isnull()
print('data.head() for salary:')
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
data["Position"]=le.fit_transform(data["Position"])
data.head()
x = data[["Position","Level"]]
y = data["Salary"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2,random_state=2)
from sklearn.tree import DecisionTreeRegressor
dt = DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred = dt.predict(x_test)
print('MSE value:')
from sklearn import metrics
mse = metrics.mean_squared_error(y_test,y_pred)
mse
print('r2 value:')
r2 = metrics.r2_score(y_test,y_pred)
r2
print('data prediction:')
dt.predict([[5,6]])
```

## Output:
## data.head()
![Screenshot 2023-11-09 081640](https://github.com/dilipkumar1265/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119065291/b7b1596f-85c3-4a29-9ac7-67799cf26add)
## data.info()
![Screenshot 2023-11-09 081650](https://github.com/dilipkumar1265/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119065291/0d05a282-6268-41e0-8a6c-65d11ac5631b)
## isnull()&sum()
![Screenshot 2023-11-09 081704](https://github.com/dilipkumar1265/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119065291/9fcaae89-8b67-4a65-9d11-d991e82e5ea1)
## data.head() for position
![Screenshot 2023-11-09 081714](https://github.com/dilipkumar1265/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119065291/a2178f3f-e3cb-4cf5-beca-7e130b23c17c)
## MSE value
![Screenshot 2023-11-09 081720](https://github.com/dilipkumar1265/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119065291/a8c1fe48-aaca-4f17-8d09-7921be859327)
## R2 value()
![Screenshot 2023-11-09 081726](https://github.com/dilipkumar1265/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119065291/528478a1-da98-44c6-912b-bdc03c44109b)
## Prediction value
![Screenshot 2023-11-09 081731](https://github.com/dilipkumar1265/Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee/assets/119065291/60641c77-c3a6-4484-9915-d7c6bd927a06)


## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
