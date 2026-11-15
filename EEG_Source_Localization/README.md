# EEG Source Localization

## Topic premise

EEG source localization is an inverse problem. A forward model maps activity
at many possible brain sources to a smaller set of scalp-electrode readings;
source localization tries to reverse that mapping. Because there are more
possible sources than independent measurements, and measurement noise is
present, many source patterns can explain nearly the same EEG data. Directly
fitting the measurements can therefore produce unstable estimates.

Regularization stabilizes this underdetermined fit by balancing data error
against a constraint on the source estimate. Ridge regression penalizes the
squared size of the coefficients, while LASSO penalizes their absolute size
and can drive some coefficients to zero, favoring a sparse solution. The
regularization strength controls the tradeoff between matching the sensor data
and restricting the estimated sources.

## Python code

[`Code/lab_eeg_partial.ipynb`](Code/lab_eeg_partial.ipynb) is a notebook
exercise. It loads the EEG forward-model data, prepares training and test
samples, fits regularized regressors, and compares their reconstruction
performance. The TODOs cover data dimensions and splitting, Ridge and LASSO
fits, model evaluation, and visualization of estimated sources.