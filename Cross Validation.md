# Cross Validation
Experimenting with different arrangement of same data to build different models of same algorithum.

Benfits :
- Model will be robust/generalized.

## Types:
### 1. Leane one out Cross Validation (LOOCV)

Disadventage:
- Model overfitting.

### 2. Leave P out Cross Validation

### 3. K-Fold Cross Validation
K-Fold Cross-Validation is a popular technique used in machine learning to evaluate the performance of a model. It involves dividing the dataset into k equally sized folds (subsets). The model is trained k times, each time using a different fold as the validation set and the remaining k-1 folds as the training set. This process helps to ensure that every data point has a chance to be in the training and validation sets, providing a more reliable measure of the model's performance.

Here’s a step-by-step explanation of K-Fold Cross-Validation:

1. Split the Data: Divide the dataset into k equally sized (or nearly equal) folds.
2. Training and Validation:
- For each fold, treat it as the validation set and combine the remaining k-1 folds as the training set.
- Train the model on the training set.
- Evaluate the model on the validation set and record the performance metric (e.g., accuracy, mean squared error).
3. Repeat: Repeat step 2 for each fold.
4. Aggregate Results: Calculate the average performance metric across all k folds to get an overall performance estimate.

This method helps to mitigate issues like overfitting and provides a more accurate assessment of the model’s ability to generalize to unseen data.

### 4. Stratified K-Fold Cross Validation
Stratified K-Fold Cross-Validation is a variation of K-Fold Cross-Validation that ensures each fold has a representative proportion of classes, making it particularly useful for imbalanced datasets. In standard K-Fold Cross-Validation, the data is split randomly, which may result in some folds having a significantly different class distribution compared to the overall dataset. Stratified K-Fold addresses this issue by preserving the percentage of samples for each class.

Key Steps in Stratified K-Fold Cross-Validation
1. Split the Data: Divide the dataset into k folds such that each fold maintains the class distribution of the original dataset.

2. Training and Validation:
- For each fold, treat it as the validation set and combine the remaining k-1 folds as the training set.
- Train the model on the training set.
- Evaluate the model on the validation set and record the performance metric (e.g., accuracy, mean squared error).

3. Repeat: Repeat step 2 for each fold.
4. Aggregate Results: Calculate the average performance metric across all k folds to get an overall performance estimate.
