# Hyper Parameter Tuning

*Hyper Parameter* : Exteranl configuration of a model that are not learned from the data but are set prior to training process. Unlike model parameters (which are learned from the training data), hyperparameters are set before training begins

Hyperparameter tuning is the process of optimizing the hyperparameters of a machine learning model to improve its performance.

Benefits of Hyperparameter Tuning:
- Improved Performance: Optimizes model performance by finding the best hyperparameters.
- Robustness: Ensures the model generalizes well to unseen data.
- Efficiency: Different methods (e.g., Random Search, Bayesian Optimization) offer trade-offs between exploration and computational cost.

Hyperparameter tuning is a crucial step in building effective machine learning models, as it can significantly impact the model's performance and generalization capabilities.

## Hyperparamater Tuning with Cross validation
Hyperparameter tuning with cross-validation involves using a cross-validation technique to evaluate the performance of different hyperparameter configurations systematically. This helps in selecting the best set of hyperparameters that leads to the optimal performance of the model. Combining hyperparameter tuning with cross-validation ensures that the model's performance is robust and not dependent on a particular train-test split.

1. Grid Search Cross validation
   - Exhaustively searches over a specified hyperparameter grid.
   - Evaluates all possible combinations of hyperparameters.
   - Can be computationally expensive.
   - Disadventage :
     - Time complexity increase with huge data from model training.
       
2. Randomized Search Cross validation
   - We will not see all possible combinations.
   - Out of all possible combinations- only select some randomly samples hyperparameters from specified distributions.
   - More efficient than grid search when the number of hyperparameters is large.

Benefits of Hyperparameter Tuning with Cross-Validation:
- Robust Performance Estimate: Cross-validation provides a more reliable estimate of the model's performance by averaging results over multiple splits.
- Optimal Hyperparameters: Systematically searches for the best hyperparameters that lead to optimal model performance.
- Generalization: Reduces the risk of overfitting by ensuring that the hyperparameter tuning process considers different subsets of the data.

## Summary
Hyperparameter tuning with cross-validation is a powerful approach to improving the performance and generalization of machine learning models. By systematically evaluating different hyperparameter configurations using cross-validation, you can identify the best settings that lead to the optimal performance of your model.
