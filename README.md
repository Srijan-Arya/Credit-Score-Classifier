# Credit Score Classification Model 🏦📊

## 📜 Overview

This project is designed to build and evaluate machine learning models for predicting credit scores. The goal is to classify credit scores into different categories based on a dataset that has undergone preprocessing to handle missing values and ensure quality.

## 📊 Dataset

The dataset used for this project is the [Credit Score Classification Dataset](https://www.kaggle.com/datasets/parisrohan/credit-score-classification) from Kaggle. This dataset includes various features related to credit scores and has been preprocessed for consistency.

## 🛠️ Models

Two powerful classification models have been implemented and evaluated:

1. **Random Forest Classifier** 🌲
2. **Gradient Boosting Classifier** 🚀

### Model Training

#### Random Forest Classifier 🌲

- **Hyperparameters Tuned**:
  - `n_estimators`: Number of trees in the forest
  - `max_features`: Number of features to consider for splitting
  - `max_depth`: Maximum depth of the trees
  - `criterion`: The function to measure the quality of a split (`gini` or `entropy`)

- **Best Parameters**:
  - `n_estimators`: 300
  - `max_features`: 'auto'
  - `max_depth`: 10
  - `criterion`: 'entropy'

#### Gradient Boosting Classifier 🚀

- **Hyperparameters Tuned**:
  - `n_estimators`: Number of boosting stages to be run
  - `learning_rate`: Shrinks the contribution of each tree
  - `max_depth`: Maximum depth of the individual trees

- **Best Parameters**:
  - `n_estimators`: 150
  - `learning_rate`: 0.1
  - `max_depth`: 4

## 📈 Model Evaluation

The models have been evaluated using various metrics:

- **Accuracy**:
  - **Random Forest**: 72.98%
  - **Gradient Boosting**: 73.17%

- **ROC-AUC Score**:
  - **Random Forest**: 0.873
  - **Gradient Boosting**: 0.874

- **Confusion Matrix**:
  - **Random Forest**:
    ```
    [[ 4044    82  1196]
     [  678  6030  2097]
     [ 2229  1824 11820]]
    ```

  - **Gradient Boosting**:
    ```
    [[ 3763    86  1473]
     [  493  5982  2330]
     [ 1764  1902 12207]]
    ```

- **Classification Report**:
  - **Random Forest**:
    ```
                   precision    recall  f1-score   support

               0       0.58      0.76      0.66      5322
               1       0.76      0.68      0.72      8805
               2       0.78      0.74      0.76     15873

        accuracy                           0.73     30000
       macro avg       0.71      0.73      0.71     30000
    weighted avg       0.74      0.73      0.73     30000
    ```

  - **Gradient Boosting**:
    ```
                   precision    recall  f1-score   support

               0       0.63      0.71      0.66      5322
               1       0.75      0.68      0.71      8805
               2       0.76      0.77      0.77     15873

        accuracy                           0.73     30000
       macro avg       0.71      0.72      0.71     30000
    weighted avg       0.73      0.73      0.73     30000
    ```

## 🚀 Getting Started

To get started with this project:

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/yourusername/credit-score-classification.git
