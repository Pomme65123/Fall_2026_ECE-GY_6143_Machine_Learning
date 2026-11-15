# Nonlinear Least Squares for Modeling Materials

## Topic premise

Least squares estimates model parameters by minimizing the sum of squared
residuals between observed values and model predictions. In nonlinear least
squares, the model can be nonlinear in its parameters, so there may be no
closed-form solution. The objective can also have local minima, making
initial parameter values and the optimization method important.

The lab fits a rational function to material data. It first obtains a useful
starting estimate, then improves the parameters by following the loss
gradient. Gradient descent uses step sizes to control each update; momentum
uses information from previous updates to help smooth and accelerate progress.
The resulting fitted curve is assessed against observed data.

## Python code

[`code/lab_nlls_partial.ipynb`](code/lab_nlls_partial.ipynb) is a notebook
exercise. It loads and scales the material data, creates training and test
sets, constructs an initial rational-model fit, and defines the nonlinear loss
and its gradient.