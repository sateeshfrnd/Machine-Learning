# Regression 

Regression is a type of supervised learning technique used for predicting a continuous outcome or dependent variable (Y) 
based on one or more independent variables (X). 
In simpler terms, regression models try to predict a value within a continuous range.

## Types of Regression in Machine Learning

1. Simple Linear Regression
2. Multiple Linear Regression
3. Polynomial Regression
4. Ridge Regression
5. Lasso Regression
6. ElasticNet Regression

### 1. Simple Linear Regression

Simple Linear Regression is the most basic form of regression. 
It assumes a linear relationship between the independent variable (X) and the dependent variable (Y).

The equation for simple linear regression is:

![image](https://github.com/user-attachments/assets/ced783ad-e68c-4573-a5f1-6bf25a69a9b1)

Where:
- Y is the dependent variable (target),
- X is the independent variable (predictor),
- ![image](https://github.com/user-attachments/assets/1662f734-d9c1-42bf-9d17-d252fe3efb97) is the intercept,
- ![image](https://github.com/user-attachments/assets/ece00fbf-51fe-4717-b502-e372d813d3d0) is the slope (coefficient), and
- ![image](https://github.com/user-attachments/assets/a181e537-5c1a-4b78-ac66-3d7e99b59ac9) is the error term.

**Example:**
We predict someone's weight based on their height.

- **Input (X)**: Height (in cm)
- **Output (Y)**: Weight (in kg)

If we have data for height and weight, a simple linear regression model will try to find 
the best-fitting straight line that predicts weight from height.

---

### 2. Multiple Linear Regression

Multiple Linear Regression extends simple linear regression by using multiple independent 
variables to predict a dependent variable. 

The equation for multiple linear regression is:

![image](https://github.com/user-attachments/assets/934661ab-0d45-4426-b444-d7ea3353761c)

Where:
- Y is the dependent variable,
- X1, X2, ..., Xn are the independent variables,
- ![image](https://github.com/user-attachments/assets/774c6098-4cdc-4e33-b250-d8789a1ff333) is the intercept,
- ![image](https://github.com/user-attachments/assets/202283b5-dc32-4d37-b8ea-0c250913fda4) are the coefficients for each independent variable, and
- ![image](https://github.com/user-attachments/assets/a181e537-5c1a-4b78-ac66-3d7e99b59ac9) is the error term.

**Example:**
You may predict the price of a house based on various features such as:
- Size of the house
- Number of rooms
- Location
- Age of the house

This can be done using multiple linear regression, where each of these features (X1, X2, ...) 
will be used to predict the target variable (Y) — the price of the house.

---

### 3. Polynomial Regression

Polynomial Regression is used when the relationship between the independent variable and the dependent variable 
is not linear but follows a polynomial relationship. 
It is an extension of linear regression that can capture the curvilinear nature of data.

The equation for polynomial regression is:

![image](https://github.com/user-attachments/assets/c284a1e7-bc62-4f60-9902-19140ba456fa)


Where:
- Y is the dependent variable,
- X is the independent variable, and
- The higher powers of X are included to capture the non-linear relationship.

**Example:**
If you have data of temperature and ice cream sales, and the relationship between them 
shows a curve (i.e., sales increase with temperature up to a point and then start to decline), 
polynomial regression can be used to model this non-linear relationship.

---

### 4. Ridge Regression

Ridge Regression is a regularization technique that adds a penalty to the coefficients in linear regression, 
which helps prevent overfitting. It is useful when there is multicollinearity (high correlation between predictors).

The equation is:

![image](https://github.com/user-attachments/assets/ae69b5e4-ec1b-4cbf-9b74-2d024421bb49)


Where:
- ![image](https://github.com/user-attachments/assets/8dc791c6-5ca4-43fa-9935-59351ae20a58)
 is the regularization parameter (higher values increase the penalty).

**Example:**
Ridge regression can be used in a dataset with multiple features 
(e.g., house price prediction with many correlated features like size, number of rooms, etc.) to prevent overfitting.

---

### 5. Lasso Regression

Lasso Regression (Least Absolute Shrinkage and Selection Operator) is another regularization technique 
that can be used for feature selection. It adds a penalty to the absolute values of the coefficients, 
forcing some of the coefficients to be exactly zero, which effectively removes less important features.

The equation is:

![image](https://github.com/user-attachments/assets/ec37bd24-56e1-41d9-a5bf-807b6171edb7)


**Example:**
Lasso regression can be used in a dataset where you have many predictors and you want to select the most relevant ones while avoiding overfitting.

---

### 6. ElasticNet Regression

ElasticNet Regression is a hybrid of Ridge and Lasso Regression. It combines both L1 (Lasso) and L2 (Ridge) penalties, 
balancing between regularization and feature selection.

The equation is:

![image](https://github.com/user-attachments/assets/28d77187-fc9e-4ae2-9210-b4d57d1468cc)

Where:
- ![image](https://github.com/user-attachments/assets/71bd8e96-4a3f-4bdc-8f26-7899504cbf5f)
 and ![image](https://github.com/user-attachments/assets/a5ff0fe8-be7c-4ad2-8cd6-5818090732f5)
 are the regularization parameters.

**Example:**
ElasticNet regression can be useful in situations where the dataset has a mix of highly correlated 
and less important features.

---

## Summary

- **Regression** in machine learning is used for predicting continuous values.
- **Simple Linear Regression** assumes a straight-line relationship, while **Multiple Linear Regression** extends this to multiple features.
- **Polynomial Regression** is used when the relationship is non-linear.
- **Ridge, Lasso, and ElasticNet** are regularization techniques to improve model performance and prevent overfitting.
