# Implementation-of-Decision-Tree-Regressor-Model-for-Predicting-the-Salary-of-the-Employee

## AIM:
To write a program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Import the standard libraries.
2. Upload the dataset and check for any null values using .isnull() function.
3. Import LabelEncoder and encode the dataset.
4. Import DecisionTreeRegressor from sklearn and apply the model on the dataset.
5. Predict the values of arrays.
6. Import metrics from sklearn and calculate the MSE and R2 of the model on the dataset.
7. Predict the values of array.
8. Apply to new unknown values.

## Program:
```

Program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee.
Developed by: MUTHUAKASH M
RegisterNumber:  212225230194

```
```
import pandas as pd
import matplotlib.pyplot as plt
data=pd.read_csv("Salary.csv")
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
from sklearn import metrics
r2=metrics.r2_score(y_test,y_pred)
r2
dt.predict([[5,6]])
```

## Output:
<img width="458" height="249" alt="image" src="https://github.com/user-attachments/assets/e7c20045-ade4-4c2a-896b-2d6ca03d8aa6" />

<img width="428" height="264" alt="image" src="https://github.com/user-attachments/assets/981d12e8-70ec-43b6-81a1-2d829efc27b8" />

<img width="358" height="258" alt="image" src="https://github.com/user-attachments/assets/977bda3c-34da-4c17-8081-36142dcb997d" />

<img width="364" height="49" alt="image" src="https://github.com/user-attachments/assets/ba49658a-db47-4fb1-83c6-aafa3ebd694a" />

<img width="285" height="45" alt="image" src="https://github.com/user-attachments/assets/a0f59c50-3f0e-42ce-802d-d48c3b01a858" />

<img width="1811" height="79" alt="image" src="https://github.com/user-attachments/assets/9de469e5-b7b2-43cc-a230-6a160eb7abd4" />

## Result:
Thus the program to implement the Decision Tree Regressor Model for Predicting the Salary of the Employee is written and verified using python programming.
