# Hyperparameter Tuning Analysis

## Experiment 7

This experiment compares a baseline Decision Tree model with
Grid Search and Random Search hyperparameter tuning for a
Random Forest classifier.

## Dataset

The experiment uses the Iris dataset stored in:

`data/processed/iris_features.csv`

The dataset contains 150 samples and 4 input features:

- sepal length
- sepal width
- petal length
- petal width

The target column is `target`.

## Baseline Model

The baseline model is a Decision Tree Classifier using default
hyperparameters.

Results:

- CV F1 Macro: 0.9413
- Test Accuracy: 0.9333
- Total Fits: 5

## Grid Search

Grid Search was performed using a Random Forest Classifier.

The search evaluated multiple combinations of:

- `n_estimators`
- `max_depth`
- `min_samples_split`
- `max_features`

Results:

- CV F1 Macro: 0.9582
- Test Accuracy: 0.9667
- Total Fits: 360

Best parameters:

```text
max_depth = 3
max_features = sqrt
min_samples_split = 2
n_estimators = 50