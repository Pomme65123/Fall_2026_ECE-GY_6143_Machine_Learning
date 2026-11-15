# Logistic Regression for Gene Expression

## Topic premise

Logistic regression is a supervised-learning method for classification. For
two classes, it applies the logistic (sigmoid) function to a weighted sum of
the input features to estimate the probability of one class. The weights are
learned by minimizing a classification loss, commonly the negative
log-likelihood (cross-entropy); a decision threshold turns the probability
into a predicted label. Multiclass problems extend this idea to estimate
probabilities for several classes.

Gene-expression data often has many features relative to the number of
samples. This makes overfitting a concern. Cross-validation estimates how
well a model may perform on new samples, and L1 regularization penalizes large
weights while encouraging some to become zero. This can simplify the model,
though the selected features should not automatically be interpreted as
causal.

## Python code

[`Code/lab_gene_partial.ipynb`](Code/lab_gene_partial.ipynb) is a notebook
exercise. It loads and prepares the gene-expression data, creates training and
test sets, fits logistic-regression classifiers, and evaluates their
predictions. Later sections inspect the learned weights, use cross-validation,
extend the task to multiple classes, and apply L1 regularization.