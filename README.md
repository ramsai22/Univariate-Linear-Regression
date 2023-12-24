# Implementation of Univariate Linear Regression
## Aim:
To implement univariate Linear Regression to fit a straight line using least squares.
## Equipment’s required:
1.	Hardware – PCs
2.	Anaconda – Python 3.7 Installation / Moodle-Code Runner
## Algorithm:
1.	Get the independent variable X and dependent variable Y.
2.	Calculate the mean of the X -values and the mean of the Y -values.
3.	Find the slope m of the line of best fit using the formula.
 ![eqn1](./eq1.jpg)
4.	Compute the y -intercept of the line by using the formula:
![eqn2](./eq2.jpg)  
5.	Use the slope m and the y -intercept to form the equation of the line.
6.	Obtain the straight line equation Y=mX+b and plot the scatterplot.
## Program
```
#Program to implement univariate Linear Regression to fit a straight line using least squares.
#Developed by: paida ram sai
#register number: 23007931

import numpy as np 
import matplotlib.pyplot as plt
x = np.array([0,1,2,3,4,5,6,7,8,9])
y = np.array([1,3,2,5,7,8,8,9,10,12])
plt.scatter(x,y)
plt.show()
xmean = np.mean(x)
ymean = np.mean(y)
num=0
den=0
for i in range(len(x)):
    num+=(x[i]-xmean)*(y[i]-ymean)
    den+=(x[i]-xmean)**2
m = num/den
b = ymean - m*xmean
print(m,b)
ypred = m*x+b
print(ypred)

plt.scatter(x,y,color='Red')
plt.plot(x,ypred,color='Blue')
plt.show()

```
## Output
![image](https://github.com/ramsai22/Univariate-Linear-Regression/assets/150319855/7c372ae0-167a-44d3-92a4-4961f652b5f3)
![image](https://github.com/AzeezBT/Univariate-Linear-Regression/assets/150319523/b61a0ce8-a4e9-4e69-84b3-7ffe8b42ad56)
![image](https://github.com/AzeezBT/Univariate-Linear-Regression/assets/150319523/67e96a00-b842-4438-a7e8-9db80e2ce59d)


## Result
Thus the univariate Linear Regression was implemented to fit a straight line using least squares.
