# Support Vector Machines on Extended MNIST

## Topic premise

Support vector machines (SVMs) are classification models that seek a decision
boundary with a wide margin between classes. In a soft-margin SVM, violations
of that boundary are allowed but penalized; the parameter `C` controls the
tradeoff between a wider margin and fewer training errors. A kernel lets the
classifier represent nonlinear boundaries without explicitly constructing
features in a high-dimensional space. For an RBF kernel, `gamma` controls how
local each training example's influence is.

The margin, `C`, and kernel settings affect how well the classifier handles
unseen examples, so parameters should be selected using validation data rather
than training accuracy alone. The lab uses EMNIST handwritten digits and
letters to practice classification, error analysis, and parameter selection.

## Python code

[`code/lab_emnist_partial.ipynb`](code/lab_emnist_partial.ipynb) is a notebook
exercise. It downloads and loads EMNIST data, prepares and rescales digit and
letter examples, trains a support vector classifier, and evaluates test
errors and a confusion matrix.