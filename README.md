# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import pandas
2. Import Decision tree classifier
3. Fit the data in the model
4. Find the accuracy score 

## Program:
```
/*
Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: RAHUL S 
RegisterNumber: 212224040259
*/
```
```
import pandas as pd
df=pd.read_csv("/content/Employee.csv")
print("data.head():")
df.head()
```
```
print("data.info()")
df.info()
```
```
print("data.isnull().sum()")
df.isnull().sum()
```
```
print("data value counts")
df["left"].value_counts()
```
```
from sklearn.preprocessing import LabelEncoder
le=LabelEncoder()
print("data.head() for Salary:")
df["salary"]=le.fit_transform(df["salary"])
df.head()
```
```
print("x.head():")
x=df[["satisfaction_level","last_evaluation","number_project","average_montly_hours","time_spend_company","Work_accident","promotion_last_5years","salary"]]
x.head()
```
```

y=df["left"]
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=100)
from sklearn.tree import DecisionTreeClassifier
dt=DecisionTreeClassifier(criterion="entropy")
dt.fit(x_train,y_train)
y_pred=dt.predict(x_test)
y_pred
```
```

from sklearn.metrics import accuracy_score
accuracy=accuracy_score(y_test,y_pred)
accuracy
```
```
print("Data prediction")
dt.predict([[0.5,0.8,9,260,6,0,1,2]])
```
```

from sklearn.tree import plot_tree
import matplotlib.pyplot as plt
plt.figure(figsize=(10,10))
plot_tree(dt,filled=True,feature_names=x.columns,class_names=['salary' , 'left'])
plt.show()
```

  


## Output:
![image](https://github.com/user-attachments/assets/729f156a-2aa9-4d44-a881-11aa0ee8b4b2)
![image](https://github.com/user-attachments/assets/e59695a1-040c-4334-a87c-2d7bff338ad3)
![image](https://github.com/user-attachments/assets/54891a24-e47c-4470-9d52-11f394d7ea38)
![image](https://github.com/user-attachments/assets/27216ab2-c2c8-4c75-90b3-b9111435a84f)
![image](https://github.com/user-attachments/assets/a1031a8a-6a2f-4edb-afe4-771ba7f501ae)
![image](https://github.com/user-attachments/assets/c1e7f6e6-ceaa-446a-8f82-a0294f4c8130)
![image](https://github.com/user-attachments/assets/8accd484-eaea-44e2-814a-1708afd982b9)
![image](https://github.com/user-attachments/assets/3c77533f-79e3-4580-a772-1e03bafff350)
![image](https://github.com/user-attachments/assets/bea65cf4-8c8c-40e6-930d-47d650fed8cc)
![image](https://github.com/user-attachments/assets/6c9ac447-f3b2-4049-ac26-f0eab4250f37)












## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
