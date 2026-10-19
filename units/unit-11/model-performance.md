# Model Performance Measurement — Unit 11

## Overview

This practical activity explored how to evaluate machine learning models using classification and regression metrics. I used Scikit-learn to calculate performance measures, generate a confusion matrix, examine classification reports, and evaluate ROC-AUC and regression errors.

## 1. Confusion Matrix

I used a confusion matrix to compare actual labels with predicted labels. For the binary example, Scikit-learn returned:

True negatives (TN): 0

False positives (FP): 2

False negatives (FN): 1

True positives (TP): 1

This showed that the model made several incorrect predictions. A confusion matrix helps identify the types of errors a classifier makes, rather than reporting only the number of correct predictions.

## 2. Classification Metrics

The activity explored accuracy, precision, recall, F1-score, ROC-AUC and log loss.

In one example, the classification report returned an overall accuracy of 0.60, a macro-average F1-score of approximately 0.49, and a weighted-average F1-score of approximately 0.61. Class 1 had precision, recall and F1-score of zero, while Class 2 had an F1-score of 0.80.

This demonstrated that reasonable overall accuracy does not necessarily mean that a model performs well for every class.

The activity also compared different F1-score averaging methods. Macro averaging gives each class equal weight, while weighted averaging accounts for the number of examples in each class. Micro averaging aggregates the contributions of individual predictions. The choice of metric should reflect the classification problem and the consequences of errors.

The notebook also calculated ROC-AUC values of approximately 0.995 for the breast cancer dataset and 0.991 for the Iris dataset. These results illustrated how AUC can be used to assess a model's ability to distinguish between classes. However, these particular scores were calculated using the same datasets used to fit the models, so they should not be treated as reliable estimates of performance on unseen data.
3. Regression Metrics

The regression section evaluated prediction errors using mean squared error (MSE), mean absolute error (MAE) and the coefficient of determination ((R^2)).

The results were:

** Mean squared error (MSE) **:0.375

** Mean squared error (MSE) **:0.500

** (R^2) **:0.9486


The mean absolute error represents the average absolute difference between actual and predicted values. Mean squared error penalises larger errors more heavily because the differences are squared. The (R^2) score indicates how well the predictions explain variation in the target values in this example.

Although the notebook section was labelled RMSE, the code calculated MSE, not root mean squared error. The corresponding RMSE would be approximately 0.6124.

## Reflection
This activity strengthened my understanding of selecting evaluation metrics according to the task being performed. Classification metrics help assess different aspects of categorical predictions, while regression metrics measure the magnitude of numerical prediction errors.

I also learned that evaluation results must be interpreted carefully. Class imbalance can make overall accuracy misleading, and evaluating a model on the same data used for training can produce overly optimistic results. For more reliable evaluation, I would use separate training, validation and test sets, examine class-level performance, and select metrics that reflect the practical consequences of prediction errors.

These lessons are relevant to my TrashNet machine learning project, where comparing accuracy, precision, recall and F1-score helped explain why the HOG-SVM model performed better overall than the CNN in my experiments, while individual classes showed different patterns of performance.## Results

## Evidence
 Practical notebook: Unit11_model_Performance_Measurement.ipynb

Source: Scikit-learn metrics and example datasets used in the Unit 11 activity.
