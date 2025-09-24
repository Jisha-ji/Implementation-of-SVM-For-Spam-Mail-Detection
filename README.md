# Implementation-of-SVM-For-Spam-Mail-Detection

## AIM:
To write a program to implement the SVM For Spam Mail Detection.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1.Data Preparation: Load and handle the dataset, separating features and target variables.
2.Data Splitting: Split the dataset into training and testing sets.
3.Feature Engineering: Transform text data into numerical feature vectors.
4.Model Building and Evaluation: Initialize SVM classifier, train the model, and predict target labels for evaluation. 

## Program:
```

Program to implement the SVM For Spam Mail Detection..
Developed by: JISHA BOSSNE SJ
RegisterNumber:  212224230106

```
```
import pandas as pd
data=pd.read_csv('C:/Users/admin/Downloads/printed pdfs/spam.csv',encoding="Windows-1252")
from sklearn.model_selection import train_test_split

data

data.shape

x=data['v2'].values

y=data['v1'].values

x.shape

y.shape

x_train, x_test, y_train, y_test = train_test_split(x,y,test_size=0.35, random_state=0)

x_train

x_train.shape

from sklearn.feature_extraction.text import CountVectorizer
cv = CountVectorizer()

x_train = cv.fit_transform(x_train)
x_test = cv.transform(x_test)

from sklearn.svm import SVC

svc=SVC()

svc.fit(x_train, y_train)

y_pred=svc.predict(x_test)

y_pred

from sklearn.metrics import accuracy_score, confusion_matrix, classification_report

acc=accuracy_score(y_test, y_pred)
acc

con=confusion_matrix(y_test,y_pred)
print(con)

cl=classification_report(y_test,y_pred)
print(cl)
```
## Output:

## Data:

<img width="744" height="448" alt="329268661-0a86ceb6-1c87-4108-a09b-7172f60caed3" src="https://github.com/user-attachments/assets/e201865c-3ded-4ed9-bd08-0aec4ed6d2c5" />

## Data Shape:

<img width="142" height="37" alt="329268865-b94e824f-74ab-48e3-8ac7-2aead572c4b4" src="https://github.com/user-attachments/assets/f2b02feb-4d83-47db-8cf8-72ce6e46fbd0" />

## x_shape:

<img width="121" height="41" alt="329268977-63dd570e-9992-472b-a2de-c66c7a86c836" src="https://github.com/user-attachments/assets/a5f14183-9ac1-4339-a752-8b9a364c3be7" />

## y_shape:

<img width="122" height="41" alt="329269142-85f0aa79-3cbc-4f2a-b84b-16d3f5956b89" src="https://github.com/user-attachments/assets/768daf93-9541-419d-9e1e-87a4c7257d91" />

## x_train:

<img width="1239" height="215" alt="329269326-9cce3e36-5496-4282-9255-882010f62405" src="https://github.com/user-attachments/assets/a570d92c-0303-4d89-9d23-068260f124c8" />

## x_train.shape:

<img width="101" height="35" alt="329269506-f586b0ec-d30b-4fa5-9c0c-94b3daf8c19a" src="https://github.com/user-attachments/assets/e50e01da-12ff-4e65-8983-c7d3add3a0d4" />

## y_pred:

<img width="775" height="66" alt="Screenshot 2025-09-24 104354" src="https://github.com/user-attachments/assets/6b6fabea-ebca-4ebb-b8d3-572a902883e5" />

## accuracy:

<img width="221" height="35" alt="Screenshot 2025-09-24 104444" src="https://github.com/user-attachments/assets/bc6b8878-8888-4877-9712-68de6ba3ca01" />

## confusion matrix:

<img width="190" height="91" alt="Screenshot 2025-09-24 104526" src="https://github.com/user-attachments/assets/34ffa7ee-2d46-467e-be3e-4dc1187ebc95" />

## classification report:

<img width="695" height="223" alt="Screenshot 2025-09-24 104534" src="https://github.com/user-attachments/assets/26275e0d-6099-4369-974b-863926b0119c" />


## Result:
Thus the program to implement the SVM For Spam Mail Detection is written and verified using python programming.
