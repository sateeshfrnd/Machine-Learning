# Evaluating Regression Models

Once we train a regression model, we need to evaluate its performance using different metrics:

1. **Mean Absolute Error (MAE)**:
   - Measures the average of the absolute errors between predicted and actual values.
        ![image](https://github.com/user-attachments/assets/3e1ead37-9d37-4227-836f-ab8547633c4a)


2. **Mean Squared Error (MSE)**:
   - Measures the average of the squared errors. It penalizes large errors more than MAE.

       ![image](https://github.com/user-attachments/assets/b3d7bc6e-5749-4472-9f82-72357500f5df)


3. **Root Mean Squared Error (RMSE)**:
   - The square root of the MSE. It gives a more interpretable metric in the same unit as the target variable.

      ![image](https://github.com/user-attachments/assets/84f9eaa2-86d4-4b2f-a883-ee09d737b2cb)


4. **R-squared (R²)**:
   - Measures the proportion of the variance in the dependent variable that is predictable from the independent variables.
     
      ![image](https://github.com/user-attachments/assets/58a112c5-ff9a-45b4-9059-fe62b73900c2)

   - An R² value close to 1 indicates a good fit.



## Summary
- Evaluating regression models is crucial to check if the model generalizes well to new data.

