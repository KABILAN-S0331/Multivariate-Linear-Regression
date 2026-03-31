# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1:
<br>Start the program and import the NumPy library.

### Step2:
<br>Input the data arrays: Weight, Volume, and CO2.

### Step3:
<br>Form the input matrix X by combining Weight and Volume, and add a column of ones for the intercept.

### Step4:
<br>Compute regression coefficients using the normal equation:
<br>β = (XᵀX)⁻¹ XᵀY

### Step5:
<br>Display the coefficients and intercept, then predict CO2 for new input values.
## Program:
```
Developed by :Kabilan S
Register no : 212225230119

import numpy as np
import matplotlib.pyplot as plt
X = np.array(eval(input()))
Y = np.array(eval(input()))
Xmean = np.mean(X)
Ymean = np.mean(Y)
num,den = 0,0
for i in range(len(X)):
    num += (X[i]-Xmean)*(Y[i]-Ymean)
    den += (X[i]-Xmean)**2
m = num/den
c = Ymean-m*Xmean
print (m, c)
Y_pred = m*X + c
print (Y_pred)
plt.scatter(X,Y)
plt.plot(X,Y_pred,color="red")
plt.show()
import pandas as pd
from sklearn import linear_model
df=pd.read_csv("car (1).csv")
x=df[["Volume","Weight"]]
y=df["CO2"]
regression=linear_model.LinearRegression()
regression.fit(x,y)
print(regression.coef_)
print(regression.intercept_)
print(regression.predict([[3300,1300]]))

```
## Output:
<img width="720" height="257" alt="image" src="https://github.com/user-attachments/assets/e5bbeb76-fcb2-439d-a957-eef81667cd15" />



## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
