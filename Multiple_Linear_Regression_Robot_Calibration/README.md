# Multiple Linear Regression for Robot Calibration

## Topic premise

Multiple linear regression extends the straight-line model to several input
features:

`y = beta_0 + beta_1 * x_1 + ... + beta_p * x_p + error`.

The coefficients are fit together, typically by minimizing squared prediction
errors. Each coefficient describes the model's predicted change in the
response for one feature when the other included features are held fixed.
Adding useful features can improve predictions, but fitting and evaluating on
the same observations can overstate performance, so a separate test set is
important for measuring generalization.

In this lab, joint position, velocity, acceleration, and strain measurements
are used to predict robot-joint current. A second motion experiment provides an
independent test of the model.

## Python code

[`Code/lab_robot_calib_partial.py`](Code/lab_robot_calib_partial.py) is the
Python export of the lab notebook. It uses pandas to load the robot time-series
data, NumPy and Matplotlib for calculations and plots, and scikit-learn's
`LinearRegression` to fit the model.