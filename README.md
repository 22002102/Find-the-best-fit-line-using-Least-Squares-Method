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

Developed by: SANJAY S
RegisterNumber:  212222230132
import numpy as np
import matplotlib.pyplot as plt
x =np.array(eval(input()))
y =np.array(eval(input()))

x_mean = np.mean(x)
y_mean = np.mean(y)
num,den=0,0

for i in range(len(x)):
  num +=(x[i]-x_mean)*(y[i]-y_mean)
  den += (x[i]-x_mean)**2
m=num/den
b=y_mean-m*x_mean
print(m,b)

y_predicted=m*x+b
print(y_predicted)

plt.scatter(x,y)
plt.plot(x,y_predicted,color='red')
plt.show()

```

## Output:

![ML EX01](https://user-images.githubusercontent.com/119091638/227724233-d8382e6a-8b15-4dda-9c37-3b888e378cbe.png)




## Result:

Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
