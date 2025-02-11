# Breast Cancer Prediction Using Random Forest

## Overview
This project focuses on predicting cancer using machine learning techniques. The dataset is processed and analyzed in a Jupyter Notebook, and various models are evaluated to determine their predictive performance.

Key Steps:
- Importing necessary libraries
- Loading and exploring the dataset
- Feature selection and preprocessing
- Model training and evaluation

## Loading Dataset
Dataset: https://archive.ics.uci.edu/ml/datasets/Breast+Cancer+Wisconsin+(Diagnostic)

## Splitting Dataset
Spliting the dataset by using the function train_test_split(). We need to pass 3 parameters features, target, and test_set size. Additionally we can also use random_state to select records randomly.

## Generating Model
### Hyperparameter Tuning

RandomizedSearchCV should be applied after splitting the data but before training the final model. This helps in tuning the hyperparameters using cross-validation and finding the best model configuration.

**Parameters:**
- n_estimators: Random number of trees from 50 to 200
- max_depth: Random max depth from 5 to 20
- min_samples_split: Random split values between 2 and 20
- min_samples_leaf: Random leaf values between 1 and 20
- bootstrap: Boolean values for bootstrap

## Model Evaluation

Let's estimate how accurately the classifier or model can predict the breast cancer of patients.

1. **Accuracy**: It is the ratio of correct predictions-both true positives and true negatives-among the total number of predictions.

    `Accuracy = (True Positives + True Negatives) / Total Predictions`

2. **Precision**: Precision is defined as the number of true positive predictions divided by all positive predictions of the model.

    `Precision = True Positives / (True Positives + False Positives)`

3. **Recall**: Recall is the ratio of true positive predictions against the sum of all actual positive instances. It is also known as sensitivity or true positive rate.

    `Recall = True Positives / (True Positives + False Negatives)`


4. **F1-score**: The F1-score is the harmonic mean of precision and recall. It is a more balanced measure considering both false positives and false negatives. A higher F1-score indicates a better balance between precision and recall.


    `F1-score = 2 * (Precision * Recall) / (Precision + Recall)`

## Specificity and Sensitivity

**Sensitivity *(True Positive Rate)***: Sensitivity measures the proportion of actual positives that are correctly identified by the test. 

Formula: 
    `Sensitivity = TP / (TP + FN)`
    
    Where:
    - TP = True Positives
    - FN = False Negatives

**Specificity *(True Negative Rate)***: Specificity measures the proportion of actual negatives that are correctly identified by the test. 

Formula:
    `Specificity = TN / (TN + FP)`
    
    Where:
    - TN = True Negatives
    - FP = False Positives


