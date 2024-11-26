# Lasso Regression

- **Lasso Regression** stands for **Least Absolute Shrinkage and Selection Operator**. 
- It is a type of linear regression that adds an **L1 regularization** term to the loss function. 
- The regularization term penalizes the sum of the absolute values of the model coefficients, effectively shrinking some coefficients to zero, which can eliminate irrelevant or less important features.

The loss function for Lasso Regression is:

Cost Function (Objective)=Residual Sum of Squares (RSS)+λ j=1 ∑n ∣ slope ∣

Where:
- RSS: Residual sum of squares (measures the error in predictions).
- λ : Regularization strength (hyperparameter).


## **Why Do We Need Lasso Regression?**

Lasso Regression is beneficial for several reasons:

1. **Feature Selection**:
   - By shrinking some coefficients to exactly zero, Lasso effectively performs feature selection, leaving only the most relevant predictors in the model.

2. **Handles Multicollinearity**:
   - When independent variables are highly correlated, Lasso helps by selecting one or a few relevant features instead of spreading weights across all correlated features.

3. **Reduces Overfitting**:
   - By constraining the size of the coefficients, Lasso reduces model complexity and prevents overfitting, especially when the number of features is much larger than the number of observations.

4. **Simplicity**:
   - Produces simpler models that are easier to interpret due to fewer non-zero coefficients.

## **When to Use Lasso Regression?**

1. **High Dimensional Data**: When the number of features is large, and you suspect many are irrelevant.
2. **Feature Selection**: If you want your model to automatically eliminate unnecessary variables.
3. **Preventing Overfitting**: To regularize a complex model and reduce variance.


## **Lasso Regression vs. Ridge Regression**

| **Aspect**            | **Lasso Regression**                           | **Ridge Regression**                        |
|------------------------|-----------------------------------------------|--------------------------------------------|
| **Penalty Term**       | L1 regularization (λ j=1 ∑n ∣ slope ∣ )  | L2 regularization (λ j=1 ∑n  slope^2) |
| **Feature Selection**  | Yes, shrinks some coefficients to zero         | No, all coefficients are shrunk but retained |
| **Effect**             | Produces sparse models                        | Reduces coefficient size, handles multicollinearity |
| **Use Case**           | When feature selection is important            | When multicollinearity needs to be addressed |

## Implementaion


## Key Observations in Lasso

- If λ is **too small**, Lasso behaves like regular Linear Regression (no feature elimination).  
- If λ is **too large**, the model can underfit because it may shrink coefficients of even relevant features to zero.  
- It's crucial to tune λ using techniques like **cross-validation**.

