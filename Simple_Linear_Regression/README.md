# Simple Linear Regression

## Topic premise

Simple linear regression is a supervised-learning method for predicting a
continuous outcome from one input feature. It assumes the average response can
be represented by a straight line,

`y = beta_0 + beta_1 * x + error`,

where `beta_0` is the intercept and `beta_1` is the change in predicted outcome
per unit change in the feature. Ordinary least squares chooses the coefficients
to minimize the sum of squared differences between observed and predicted
values. The fitted relationship describes association, not necessarily
causation; its usefulness is judged by how well it explains or predicts data.

The housing exercise uses number of rooms as the feature and price as the
outcome. It introduces visualization, coefficient interpretation, and the
coefficient of determination (`R^2`) as a measure of fit.

## Python code

[`Code/lab_housing_partial.ipynb`](Code/lab_housing_partial.ipynb) is a
notebook-based exercise. It loads and inspects the housing data with pandas,
uses NumPy for basic calculations, and uses Matplotlib to plot price against the
number of rooms. The exercises then fit a simple linear model, report its
coefficients and coefficient of determination, and plot the fitted line with
the observations.