# Implementation-of-SVM-For-Spam-Mail-Detection
### Name: Anbuselvan.S
### Reference No: 212223240008
## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Moodle-Code Runner

## Algorithm
1.Import the required packages.
2.Import the dataset to operate on.
3.Split the dataset.
4.Predict the required output.
5.End the program.

## Program:
```
Program to implement the SVM For Spam Mail Detection..
Developed by: Anbuselvan.S
RegisterNumber: 2122213240008
```
```
import pandas as pd
data=pd.read_csv("spam.csv",encoding='latin-1')
data.head()
data.info()
data.isnull().sum()
x=data["v1"].values
y=data["v2"].values
from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test=train_test_split(x,y,test_size=0.2,random_state=0)
from sklearn.feature_extractiaon.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred
from sklearn import metrics
accuracy=metrics.accuracy_score(y_test,y_pred)
accuracy
```

## Output:
## Data Head:
![image](https://user-images.githubusercontent.com/94165326/173095503-0b0e3fa1-b2a7-482b-b950-bc1e86f9aa82.png)

## Data Info:
![image](https://user-images.githubusercontent.com/94165326/173095546-c57eacdf-781b-4016-8c44-57e81ceb3c16.png)

## Data isnull():
![image](https://user-images.githubusercontent.com/94165326/173095639-9dc858dd-6567-43b5-811f-d9536cdc67f0.png)

## y_pred:
![image](https://user-images.githubusercontent.com/94165326/173095689-ce42426f-57c2-48ee-9541-bc6eb5622e81.png)

## Accuracy:
![image](https://user-images.githubusercontent.com/94165326/173095753-d9e9bb74-d85e-4373-9198-6cd36c476d02.png)

## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
