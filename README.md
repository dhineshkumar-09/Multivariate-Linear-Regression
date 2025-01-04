# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
Import pandas as pd and import linear_model from sklearn

### Step2
Read the csv file (saved in the same diectory) using pd.read_csv. 

### Step3
Pepare regression using linear_model.LinearRegession() and assign it to identifier "regr"

### Step4
The coefficient can be obtained by regr.coef_ and intercept can be obtained by egr.itercept_. The predicted result can be obtaied by regr.predict().

### Step5
Print the output and end the program.

## Program:
```
import pandas as pd

from sklearn import linear_model

df = pd.read_csv("carsemission.csv")

X = df[['Weight', 'Volume']]

y = df['CO2']

regr = linear_model.LinearRegression()

regr.fit(X, y)

print('Coefficients:', regr.coef_)

print('Intercept:', regr.intercept_)

input_data = pd.DataFrame({'Weight': [3300], 'Volume': [1300]})

predictedCO2 = regr.predict(input_data)

print('Predicted CO2 for the corresponding weight and volume:', predictedCO2)
```
## Output:
![Screenshot 2025-01-04 103749](https://github.com/user-attachments/assets/af0e9ca2-ed85-4d44-93a4-10bb918884ba)

## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
