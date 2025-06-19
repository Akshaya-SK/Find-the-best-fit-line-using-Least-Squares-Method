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
/*
# Program to implement univariate Linear Regression to fit a straight line using least squares.
# Developed by: Akshaya S K
# Register Number: 212223040011

import numpy as np
import matplotlib.pyplot as plt

# 1. Sample data (Independent variable X and Dependent variable Y)
X = np.array([1, 2, 3, 4, 5])      
Y = np.array([2, 4, 5, 4, 5])      

# 2. Calculate the means
mean_X = np.mean(X)
mean_Y = np.mean(Y)

# 3. Calculate the slope (m) of the line
numerator = np.sum((X - mean_X) * (Y - mean_Y))
denominator = np.sum((X - mean_X) ** 2)
m = numerator / denominator

# 4. Calculate the intercept (b)
b = mean_Y - m * mean_X

print(f"Equation of the line: Y = {m:.2f}X + {b:.2f}")

# 5. Predict Y values using the line equation
Y_pred = m * X + b

# 6. Plotting the points and the best fit line
plt.scatter(X, Y, color='blue', label='Actual data')
plt.plot(X, Y_pred, color='red', label='Best fit line')
plt.xlabel('X - Independent Variable')
plt.ylabel('Y - Dependent Variable')
plt.title('Univariate Linear Regression')
plt.legend()
plt.grid(True)
plt.show()
 
*/
```

## Output:
![image](https://github.com/user-attachments/assets/a9e88f45-9386-4170-a00a-a1e7c0f63a9b)



## Result:
Thus the univariate Linear Regression was implemented to fit a straight line using least squares using python programming.
