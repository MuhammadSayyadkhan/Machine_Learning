# 📈 Linear Regression  

Welcome to the **Linear Regression** section of this repository! 🚀  
Linear Regression is one of the most basic yet powerful algorithms in Machine Learning. It helps us **predict a continuous value** based on input data.  

---

## 🔹 What is Linear Regression?  
Linear Regression finds the **best-fit line** that shows the relationship between input (X) and output (Y).  

Think of it like drawing a straight line through data points so that it comes **as close as possible to all points**.  

---

## 🔹 Equation of a Line  

The basic formula is:  

**y = mX + c**  

- **y** → predicted value  
- **X** → input feature  
- **m** → slope of the line  
- **c** → intercept (where line crosses the Y-axis)  

---

## 🔹 Cost Function (Mean Squared Error - MSE)  

To check how well the line fits, we use a **cost function**.  
The most common one is **Mean Squared Error (MSE)**:  

\[
MSE = \frac{1}{n} \sum (y_{pred} - y_{actual})^2
\]

👉 Lower MSE means our line fits better!  

---

## 🔹 Gradient Descent  

Gradient Descent is a method to **improve the line** step by step.  
It updates the slope (**m**) and intercept (**c**) to minimize the cost function.  

- Start with random values of m and c  
- Calculate error  
- Adjust m and c slightly to reduce error  
- Repeat until the error is very small  

---

## 🔹 Types of Linear Regression  

1. **Simple Linear Regression**  
   - Only **one input feature** (X → Y).  
   - Example: Predicting **house price** from **size**.  

2. **Multiple Linear Regression**  
   - Uses **more than one input feature**.  
   - Example: Predicting **house price** using **size, number of rooms, and location**.  

---

## 🔹 Implementation in Python  

We can implement Linear Regression in two ways:  

### 1. From Scratch (with formulas & gradient descent)  

import numpy as np

### #Sample data
X = np.array([1, 2, 3, 4, 5])
Y = np.array([2, 4, 6, 8, 10])

### #Calculate slope (m) and intercept (c)
m = ((np.mean(X*Y)) - (np.mean(X)*np.mean(Y))) / ((np.mean(X**2)) - (np.mean(X)**2))
c = np.mean(Y) - m*np.mean(X)

print(f"Equation of line: y = {m}x + {c}")


---

### 2. Using Scikit-Learn


from sklearn.linear_model import LinearRegression
import numpy as np

### #Sample data
X = np.array([[1], [2], [3], [4], [5]])
Y = np.array([2, 4, 6, 8, 10])

### #Create and train model
model = LinearRegression()
model.fit(X, Y)

### #Prediction
print("Prediction for X=6:", model.predict([[6]]))


---

## 🔹 Visualizing Linear Regression

Plots help us understand better!
- 📈 Data points are shown as dots
- 📉 Best-fit line shows the predicted trend

---

import matplotlib.pyplot as plt

plt.scatter(X, Y, color="blue", label="Data Points")
plt.plot(X, model.predict(X), color="red", label="Best Fit Line")
plt.legend()
plt.show()


---

## 🎯 Key Takeaways

- Linear Regression is used for predicting continuous values.
- Equation: y = mx + c
- We use MSE to check errors.
- Gradient Descent helps optimize the line.
- Works with one feature (simple) or many features (multiple).