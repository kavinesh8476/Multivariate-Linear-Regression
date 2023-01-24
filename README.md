# Implementation of Multivariate Linear Regression
## Aim
To write a python program to implement multivariate linear regression and predict the output.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
### Step1
import pandas as pd

### Step2
read the csv file

### Step3
get the value of x and y variables

### Step4
create the linear regression model and fit

### Step5
predict the CO2 emission of a car where the weight is 2300kg and the volume is 1300cm3

### Step6

print the predicted output

## Program:
```
# Developed by:KAVINESH M
# Register no:22008476
import pandas as pd
from sklearn import linear_model
import matplotlib.pyplot as plt

df = pd.read_csv("cars.csv")

X = df[['Weight', 'Volume']]
y = df['CO2']

regr = linear_model.LinearRegression()
regr.fit(X,y)
#Cofficients and intercept of Model
print('Coefficients: ', regr.coef_) 
print('Intercept: ',regr.intercept_)

#predict the CO2 emission of a car where the weight is 300kg, and the volume is 1300cm3:
predictedCO2 = regr.predict([[3300, 1300]])
print('Predicted CO2 for the corresponding weight and volume', predictedCO2)

```
## Output:
![cars snap](https://user-images.githubusercontent.com/118466561/214367686-13b7ce0e-dc82-4fca-b1f4-8b818f700ac5.jpg)


## Result
Thus the multivariate linear regression is implemented and predicted the output using python program.
