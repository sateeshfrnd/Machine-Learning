# ElasticNet Regression
- ElasticNet Regression is a linear regression technique that combines the regularization properties of **Ridge Regression** and **Lasso Regression**. 
- It applies both (L1) (Lasso) and (L2) (Ridge) penalties to the regression model.

### Why ElasticNet Regression?
ElasticNet is useful when:
1. **Feature Selection and Shrinkage are Both Needed**:
   - Lasso may eliminate too many features in the presence of correlated variables.
   - Ridge retains all features but doesn't perform feature selection.

2. **Correlation Between Features**:
   - If predictors are highly correlated, Lasso might arbitrarily select one predictor and ignore others. ElasticNet balances this by combining (L1) and (L2) regularizations.

3. **Sparse and High-dimensional Data**:
   - When the number of predictors is much larger than the number of observations, ElasticNet works effectively.


### **Key Parameters in ElasticNet**
1. **`alpha`**:
   - Controls the overall strength of regularization.
   - Larger α  → Greater penalty → Smaller coefficients.

2. **`l1_ratio`**:
   - Balances Lasso (L1) and Ridge (L_2).
   - l1_ratio = 1 : Pure Lasso.
   - l1_ratio = 0 : Pure Ridge.
   - 0 < l1_ratio < 1 : Combination.


## Comparison with Other Methods

| **Property**      | **Ridge Regression**                     | **Lasso Regression**                    | **ElasticNet Regression**                       |
|--------------------|------------------------------------------|------------------------------------------|------------------------------------------------|
| **Penalty**        | \( \sum \beta_j^2 \) (\( L_2 \))         | \( \sum |\beta_j| \) (\( L_1 \))         | Combination: \( \lambda L_1 + (1-\lambda) L_2 \) |
| **Feature Selection** | Retains all features                  | Eliminates some features                 | Can eliminate irrelevant features               |
| **Feature Correlation** | Struggles with high correlations   | Struggles with high correlations         | Handles correlated features effectively         |

---

## When to Use ElasticNet?

1. Your dataset contains **many features**, and you suspect some are irrelevant.
2. There is **high multicollinearity** among predictors.
3. You need a **flexible and robust regularization approach**.

---

### **Experimentation**
Try varying:
- **`alpha`**: Strength of regularization.
- **`l1_ratio`**: Mix of Lasso and Ridge penalties.
