# Credit Score Classification Model 🏦📊

![image](https://github.com/user-attachments/assets/02ec4cd6-a975-4bae-8945-96ec992ef8e3)


## 📜 Project Overview

This project is designed to develop and evaluate machine learning models for classifying credit scores into distinct categories. Using a well-preprocessed dataset, we aim to build robust models to predict creditworthiness based on financial attributes. The primary focus is on achieving high performance in terms of accuracy and ROC-AUC score, a key metric for assessing the quality of multi-class classification models.

## 📊 Dataset

The dataset utilized in this project is the [Credit Score Classification Dataset](https://www.kaggle.com/datasets/parisrohan/credit-score-classification) available on Kaggle. This dataset includes various features relevant to credit scoring and has been preprocessed to handle missing values and ensure overall data quality.
![image](https://github.com/user-attachments/assets/cbdd7893-0a60-4ed9-91ad-a17ce73d0a82)

## 🛠️ Models

We have implemented and evaluated two advanced machine learning models:

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
  - `n_estimators`: Number of boosting stages to run
  - `learning_rate`: Shrinks the contribution of each tree
  - `max_depth`: Maximum depth of the individual trees

- **Best Parameters**:
  - `n_estimators`: 150
  - `learning_rate`: 0.1
  - `max_depth`: 4

## 📈 Model Evaluation

### Accuracy and ROC-AUC Score

Model performance is evaluated using multiple metrics, with a particular emphasis on the ROC-AUC score, which provides insight into the model's ability to distinguish between classes across different thresholds.

- **Random Forest Classifier** 🌲:
  - **Accuracy**: 72.98%
  - **ROC-AUC Score**: 0.873
  - **Confusion Matrix**:
    ```
    [[ 4044    82  1196]
     [  678  6030  2097]
     [ 2229  1824 11820]]
    ```
  - **Classification Report**:
    ```
                   precision    recall  f1-score   support

               0       0.58      0.76      0.66      5322
               1       0.76      0.68      0.72      8805
               2       0.78      0.74      0.76     15873

        accuracy                           0.73     30000
       macro avg       0.71      0.73      0.71     30000
    weighted avg       0.74      0.73      0.73     30000
    ```

- **Gradient Boosting Classifier** 🚀:
  - **Accuracy**: 73.17%
  - **ROC-AUC Score**: 0.874
  - **Confusion Matrix**:
    ```
    [[ 3763    86  1473]
     [  493  5982  2330]
     [ 1764  1902 12207]]
    ```
  - **Classification Report**:
    ```
                   precision    recall  f1-score   support

               0       0.63      0.71      0.66      5322
               1       0.75      0.68      0.71      8805
               2       0.76      0.77      0.77     15873

        accuracy                           0.73     30000
       macro avg       0.71      0.72      0.71     30000
    weighted avg       0.73      0.73      0.73     30000
    ```

### ROC Curve Analysis

![image](https://github.com/user-attachments/assets/e342755b-2a78-4053-85e0-fbae3b73278c)


The ROC-AUC score reflects the models' ability to distinguish between classes across various thresholds. Higher ROC-AUC scores indicate better model performance.

The ROC curves for each class are plotted to visualize the true positive rate versus the false positive rate. This helps in understanding how well each model performs in distinguishing between different credit score categories.
