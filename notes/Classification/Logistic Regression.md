# Logistic Regression

Logistic Regression is a **supervised machine learning algorithm** primarily used for **binary classification problems**, where the goal is to classify data into one of two categories

Eg: Pass vs. Fail, Spam vs. Not Spam, Disease vs. No disease.

Unlike Linear Regression, which predicts continuous values, Logistic Regression predicts **probabilities** that a given input belongs to a particular class and uses a threshold to classify inputs into discrete classes.

Logistic Regression uses the logistic (sigmoid) function to model the relationship between the independent variables (𝑋) and the dependent variable (𝑦).

The sigmoid function is defined as:

![image](https://github.com/user-attachments/assets/6dc19dce-4d80-446c-a71d-ed337faee5d2)

This output is a probability, and we classify it as:
- 𝑃(𝑦 = 1∣𝑋) ≥ 0.5 : Class 1
- 𝑃(𝑦 = 1∣𝑋) < 0.5 : Class 0

Sigmoid (logistic) function map any real-valued number into the range [0, 1]. 

```
Logistic Regression is a classification algorithm, not a regression algorithm, despite its name.
```
## Why the Name "Regression"?
- The algorithm calculates weights (𝛽0, 𝛽1, …) using a method similar to linear regression.
- However, instead of minimizing Mean Squared Error (MSE), logistic regression minimizes the log-loss or cross-entropy loss.

Logistic Regression is classification, not regression, because its primary goal is to classify data into categories based on probabilities. 

## Advantages
- Simple and Interpretable: Easy to implement and understand.
- Probabilistic Output: Provides probabilities for predictions.
- Efficient: Works well for small to medium-sized datasets.

## Disadvantages
- Linear Decision Boundary: Performs poorly if the relationship between features and labels is non-linear.
- Feature Engineering: Requires proper feature scaling and transformation.
- Sensitive to Outliers: Logistic Regression can be impacted by extreme values.

## Applications
- Healthcare: Disease diagnosis (e.g., diabetes prediction).
- Marketing: Customer churn prediction.
- Finance: Credit risk modeling.
- Email Filtering: Spam detection.
