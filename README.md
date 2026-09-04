# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. 
2. 
3. 
4. 

## Program:
```
/*
Program to implement the SVM For Spam Mail Detection..
Developed by: Swetha A
RegisterNumber:212224040343 
*/

import pandas as pd
data=pd.read_csv("spam.csv", encoding='Windows-1252')
data

data.shape

x=data['v2'].values
y=data['v1'].values
x.shape

y.shape

from sklearn.model_selection import train_test_split
x_train,x_test,y_train,y_test = train_test_split(x,y,test_size=0.2, random_state=0)
x_train

x_train.shape

from sklearn.feature_extraction.text import CountVectorizer
cv=CountVectorizer()
x_train=cv.fit_transform(x_train)
x_test=cv.transform(x_test)
from sklearn.svm import SVC
svc=SVC()
svc.fit(x_train,y_train)
y_pred=svc.predict(x_test)
y_pred

from sklearn.metrics import accuracy_score,confusion_matrix,classification_report
acc=accuracy_score(y_test,y_pred)
acc

con=confusion_matrix(y_test,y_pred)
print(con)

cl=classification_report(y_test,y_pred)
print(cl)
```

## Output:
<img width="1048" height="657" alt="447099614-33c17bad-6e14-4095-83a7-6bc3a312954a" src="https://github.com/user-attachments/assets/2a4566aa-c8a8-4874-96b6-9933080297df" />
<img width="962" height="83" alt="447099930-efc87242-c3f1-48f4-8240-edc5a3c38802" src="https://github.com/user-attachments/assets/2602dc13-9c4c-49a3-9854-4edf9f534839" />

<img width="877" height="77" alt="447100524-d1b52a4e-add4-4533-b2ec-914450655b75" src="https://github.com/user-attachments/assets/258a0e70-2271-4bb2-bfb7-005dbfd37ab5" />
<img width="873" height="265" alt="447099831-7411653b-9ca9-4ebf-9ba6-ec3f126c97bd" src="https://github.com/user-attachments/assets/cb20d9f7-8001-46e8-8bc3-451977ba70c7" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
