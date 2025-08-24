# Regression Loss Function Overview

* Enables the evaluation of model accuracy and guidance for improvements during training by indicating how the model should adjust its parameters to improve predictions
* The lower the loss the better

<br>

# Regression Loss Functions

## Mean Squared Error (MSE)

MSE (L2 Loss) is the average of squared differences between actual and predicted values 

<br>

## Mean Absolute Error (MAE)

MAE (L1 Loss) is the average of absolute differences 

<br>

## Huber Loss

* Combines MSE and MAE to be less sensitive to outliers 
* Provides a tunable threshold to switch between quadratic and linear loss