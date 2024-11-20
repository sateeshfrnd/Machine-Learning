# Overfitting vs Underfitting vs Generalization

In machine learning, the balance between underfitting, a generalized model, and overfitting is critical to building a good model. 

### Overfitting
The model learns *too much detail* from the training data, including noise. 
It performs well on the training data but poorly on unseen(validation/test) data. 

**Causes:**
- Too many features or parameters.
- Model complexity is too high.
- Training the model for too long.

**Symptoms:**
- High variance: The model is too sensitive to small fluctuations in the training data.
- Very low training error but high validation error.


### Underfitting
The model is too simple to capture the underlying patterns in the training data.
It performs poorly on both training and validation data.

**Causes**:
- The model is not complex enough (e.g., using a linear model for nonlinear data).
- Insufficient training time or too few features.

**Symptoms:**
- *High bias:* The model makes strong assumptions and cannot capture the data complexity.
- Both training and validation errors are high. 

### Generalized Model
The model captures the right patterns in the data without memorizing it (overfitting or underfitting).
It performs well on both training and unseen (validation/test) data.

**Characteristics:**
- Balanced bias and variance.
- Low training and validation errors, close to each other.

---
## Analogy
1. **Underfitting**:
   - You just skim the textbook and don’t focus on important topics.
   - Result: You fail the test because you didn’t learn enough.
   
2. **Overfitting**:
   - You memorize every single word in the textbook, even irrelevant details.
   - Result: You fail the test because the questions were different, and you couldn’t apply your knowledge.

3. **Generalization**:
   - You understand the core concepts and learn to apply them to various situations.
   - Result: You excel the test because you’ve learned what’s important and how to use it.
---
## Example: Predicting House Prices

**Dataset:**
- Features: Square footage of houses, number of rooms, etc.
- Target: House price.


**Case 1: Underfitting**
- **Model**: A simple linear model (straight line).
- **Problem**: 
  - It assumes a simple relationship between size and price but ignores more complex patterns.
  - **Training Error**: High.
  - **Validation Error**: High.
- **Example**:
  ```python
  from sklearn.linear_model import LinearRegression
  model = LinearRegression()  # Too simple for complex data
  ```

---

**Case 2: Overfitting**
- **Model**: A highly complex model, such as a 20-degree polynomial.
- **Problem**: 
  - It tries to capture every small fluctuation in the training data (noise).
  - **Training Error**: Very low.
  - **Validation Error**: High.
- **Example**:
  ```python
  from sklearn.preprocessing import PolynomialFeatures
  from sklearn.pipeline import make_pipeline
  model = make_pipeline(PolynomialFeatures(20), LinearRegression())  # Overly complex
  ```

---

**Case 3: Generalized Model**
- **Model**: A moderately complex model, such as a 2-degree polynomial.
- **Problem**: None!
  - It captures the overall trend without memorizing noise.
  - **Training Error**: Low.
  - **Validation Error**: Low.
- **Example**:
  ```python
  model = make_pipeline(PolynomialFeatures(2), LinearRegression())  # Balanced
  ```

---
## Visualization
Imagine plotting the data and the model:
1. **Underfitting**: The model (a straight line) is far from the data points.
2. **Overfitting**: The model wiggles through every data point.
3. **Generalization**: The model follows the overall trend, ignoring minor noise.

---
## Metrics to Identify
| Scenario       | Training Error | Validation Error | Generalization |
|-----------------|----------------|------------------|----------------|
| Underfitting    | High           | High             | Poor           |
| Overfitting     | Low            | High             | Poor           |
| Generalization  | Low            | Low              | Good           |


## Comparison

| **Aspect**               | **Underfitting**                          | **Generalized Model**                       | **Overfitting**                          |
|---------------------------|-------------------------------------------|---------------------------------------------|------------------------------------------|
| **Complexity**            | Too low                                   | Balanced                                    | Too high                                 |
| **Training Error**        | High                                      | Low                                        | Very low                                 |
| **Validation Error**      | High                                      | Low                                        | High                                     |
| **Bias**                  | High                                      | Balanced                                   | Low                                      |
| **Variance**              | Low                                       | Balanced                                   | High                                     |
| **Performance on Test Data** | Poor                                   | Good                                       | Poor                                     |

## How to Avoid Overfitting or Underfitting?
- **For Underfitting**:
  - Use a more complex model.
  - Add more relevant features.
  
- **For Overfitting**:
  - Reduce model complexity.
  - Use **regularization** techniques like Lasso or Ridge.
  - Increase training data.
