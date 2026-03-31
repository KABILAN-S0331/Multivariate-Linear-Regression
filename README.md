# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
###Step1:
Start the program and import the NumPy library.
###Step2:
Input the data arrays: Weight, Volume, and CO2.
###Step3:
Form the input matrix X by combining Weight and Volume, and add a column of ones for the intercept.
###Step4:
Compute regression coefficients using the normal equation:
β = (XᵀX)⁻¹ XᵀY
###Step5:
Display the coefficients and intercept, then predict CO2 for new input values.
## Program:
```
Developed by :Kabilan S
Register no : 212225230119

import numpy as np
Weight = np.array([790, 1160, 929, 865, 1140])
Volume = np.array([1000, 1200, 900, 1100, 1300])
CO2 = np.array([99, 95, 90, 97, 96])
X = np.column_stack((Weight, Volume))
X = np.c_[np.ones(X.shape[0]), X]  # add intercept
beta = np.linalg.inv(X.T @ X) @ X.T @ CO2
print("Coefficients:", beta[1:])
print("Intercept:", beta[0])
new = np.array([1, 3300, 1300])
pred = new @ beta
print("Predicted CO2:", pred)



```
## Output:
<img width="594" height="293" alt="image" src="https://github.com/user-attachments/assets/8cf04b69-eff0-4562-bf90-6b228d84421a" />


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
