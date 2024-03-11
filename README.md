# Implementation of Univariate Linear Regression
## AIM:
To implement univariate Linear Regression to fit a straight line using least squares.

## Equipments Required:
1. Hardware – PCs
2. Anaconda – Python 3.7 Installation / Jupyter notebook

## Algorithm
1. Get the independent variable X and dependent variable Y.
2. Calculate the mean of the X -values and the mean of the Y -values.
3. Find the slope m of the line of best fit using the formula. 
<img width="231" alt="image" src="https://user-images.githubusercontent.com/93026020/192078527-b3b5ee3e-992f-46c4-865b-3b7ce4ac54ad.png">
4. Compute the y -intercept of the line by using the formula:
<img width="148" alt="image" src="https://user-images.githubusercontent.com/93026020/192078545-79d70b90-7e9d-4b85-9f8b-9d7548a4c5a4.png">
5. Use the slope m and the y -intercept to form the equation of the line.
6. Obtain the straight line equation Y=mX+b and plot the scatterplot.

## Program:
```
Program to implement univariate Linear Regression to        
fit a straight line using least squares.
Developed by: Yogeshvar M
RegisterNumber:  212222230180
```
```python
import numpy as np
import matplotlib.pyplot as plt
X=np.array(eval(input("Enter the input x values in array:")))
Y=np.array(eval(input("Enter the input y values in array:")))
X_mean=np.mean(X)
Y_mean=np.mean(Y)
num=0
denom=0
for i in range(len(X)):
    num+=(X[i]-X_mean)*(Y[i]-Y_mean)
    denom+=(X[i]-X_mean)**2
m=num/denom
print("The slope of the predicted line is : ",m)
b=Y_mean - m*X_mean
print("The y-intercept is :",b)
Y_pred=m*X+b
print("The 'y' predicted values are :",Y_pred)
plt.scatter(X,Y,color='blue')
plt.plot(X,Y_pred,color='green') 
plt.show()

```

## Output:

![image](https://github.com/Yogeshvar005/Find-the-best-fit-line-using-Least-Squares-Method/assets/113497367/341ab6bd-4d8c-4b1b-8452-76bd1207fd97)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
