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
Program to implement univariate Linear Regression to fit a straight line using least squares.
### Developed by: Kailash Kumar S
### RegisterNumber: 212223220041
```python
import numpy as np
import matplotlib.pyplot as plt
x = np.array(eval(input()))
y = np.array(eval(input()))
xmean = np.mean(x)
ymean = np.mean(y)
num=0
denom=0
for i in range(len(x)):
  num+=(x[i]-xmean)*(y[i]-ymean)
  denom+=(x[i]-xmean)**2
m=num/denom
b=ymean-m*xmean
print(m,b)
y_predicted = m*x+b
print(y_predicted)
plt.scatter(x,y)
plt.plot(x,y_predicted)
plt.show()
```
### Output:
### Y-intercept
![Screenshot 2024-11-18 102111](https://github.com/user-attachments/assets/30dba2ba-701d-479d-bd7f-e5a5246593c3)
### Y_predict
![Screenshot 2024-11-18 102111](https://github.com/user-attachments/assets/89e192a1-1861-4e5c-a61a-207aa3f9bf55)
### plt.show()
![Screenshot 2024-11-18 102338](https://github.com/user-attachments/assets/3df7b30e-6f8f-4175-bff1-d1eadcd58b83)
## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
