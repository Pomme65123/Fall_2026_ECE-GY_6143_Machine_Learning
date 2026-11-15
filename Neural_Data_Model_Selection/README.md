# Model Order Selection for Neural Data

## Topic premise

In time-series prediction, a response can depend on both the current input and
its recent history. A model with delay order `d` can include the current input
and the previous `d` inputs; increasing `d` gives the model more temporal
context but also adds parameters. Too few delays can miss relevant structure
(underfitting), while too many can fit noise (overfitting).

Model-order selection uses data not used to fit each candidate model to compare
their predictive performance. Cross-validation repeats this comparison across
multiple data splits, making the choice less dependent on one particular
split. The lab applies this reasoning to predict neural responses from
stimulus history.

## Python code

[`Code/lab_neural_partial.ipynb`](Code/lab_neural_partial.ipynb) is a notebook
exercise. It loads the neural dataset, builds linear models with different
numbers of input delays, and evaluates predictive fit with held-out data and
k-fold cross-validation.