# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2. Import Decision tree regressor
3. Fit the data in the model
4. Find the accuracy score 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: RAHUL S 
RegisterNumber:  212224040259
*/
```
```
import pandas as pd
df=pd.read_csv("/content/Salary.csv")
df.head()
df.info()
df.isnull().sum()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
df["Position"]=le.fit_transform(df["Position"])
df.head()
```
```
x=df[['Position','Level']]
x.head()
y=df['Salary']
y.head()
```
```
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
```
```
from sklearn.tree import DecisionTreeRegressor
dt=DecisionTreeRegressor()
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
from sklearn.metrics import r2_score
r2=r2_score(y_test,y_pred)
r2
```
```
dt.predict([[5,6]])
```

  


## Output:
![image](https://github.com/user-attachments/assets/644df758-f1a5-4448-90cf-94d9c6aef823)
![image](https://github.com/user-attachments/assets/e6e61d23-58fc-4dd4-8df3-3f2fe6b09290)
![image](https://github.com/user-attachments/assets/01350199-bcd2-4cae-858a-8f7c09ec38c8)
![image](https://github.com/user-attachments/assets/67a785ab-424d-466d-aa97-fb51470afd8a)
![image](https://github.com/user-attachments/assets/40507576-4984-481e-8c79-75c34130e50a)

















## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
