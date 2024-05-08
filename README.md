# Cirrhosis_prediction
This repository contains a Cirrhosis patient survival outcome challenge from Kaggle.
------

## Overview
The challenge tasks participants with using a multi-class approach to predict outcomes for cirrhosis patients. Each patient's true class label (Status) needs to be predicted as one of three possibilities: Status_C, Status_CL, or Status_D. The repository's approach involves employing various machine learning algorithms to solve this multi-class classification problem. The best-performing model achieved an accuracy of 82.5%, indicating its ability to correctly predict outcomes for 82.5% of cases.

## Summary of Workdone

### Data
The data provided for this challenge is synthetic and originates from a deep learning model trained on the Cirrhosis Patient Survival Prediction dataset. It's in the form of a CSV file containing features, aimed at predicting probabilities for three outcomes: Status_C, Status_CL, and Status_D. The dataset is 1.39 MB in size and includes 5468 patients in the training set and 1368 patients in the test set.

#### Preprocessing / Clean up
* **Handling Missing Values:** Checked for missing values in the dataset. For numerical features, fill missing values with the mean or median of the respective column. For categorical features, fill missing values with the mode.
* **Outlier Detection and Removal:** Identified outliers using the z-score method and removed them to prevent skewing the model's performance.
* **Dropping Unnecessary Columns:** Dropped columns that were not useful for analysis or modeling, such as 'id' columns or columns with high cardinality.

### Feature Engineering
* **One-Hot Encoding:** Applied one-hot encoding to categorical variables to convert them into a format suitable for machine learning algorithms.
* **Box-Cox Transformation:** Performed Box-Cox transformation on numerical features to normalize their distribution.
* **Standardization:** Standardized numerical features to bring them to the same scale using StandardScaler from scikit-learn.

#### Data Visualization
![download](https://colab.research.google.com/drive/1vPtJxi-lAOCBEb3tdzdRzoh1LPqOvO9e#scrollTo=kdS6W-Lu1k60&line=2&uniqifier=1)

### Problem Formulation
  * Input: CSV file of features; Output: Predicted probabilities for each of the three possible outcomes: Status_C, Status_CL, and Status_D.
  * Models
    * Logistic Regression: A simple linear model used for binary and multi-class classification tasks. Logistic regression was chosen as it is interpretable, computationally efficient, and serves as a baseline model.
    * Random Forest: An ensemble learning method that constructs multiple decision trees during training and outputs the mode of the classes for classification tasks. Random forest was selected for its ability to handle non-linear relationships, handle categorical variables, and reduce overfitting.

### Training
The training process utilized the scikit-learn library within a Jupyter Notebook environment for code execution and analysis.
![Logistic Regression Learning curve](https://github.com/haydenBustos/Cirrhosis_prediction/assets/89792441/4406b287-b9e4-4c12-b564-ef65eefcb5fb)


### Performance Comparison

Accuracy measures the overall correctness of the predictions, precision quantifies the ratio of correctly predicted positive observations to the total predicted positives, recall measures the ratio of correctly predicted positive observations to the actual positives, and F1-score provides a harmonic mean of precision and recall.
*  ![Random Forest Learning Curve](https://github.com/haydenBustos/Cirrhosis_prediction/assets/89792441/2066a210-d6a9-429d-a81c-8aa8af90f479)


### Future Work
Model Selection: Experiment with more advanced machine learning algorithms or ensemble methods, such as gradient boosting machines (e.g., XGBoost, LightGBM) or neural networks, to improve predictive performance.

### Overview of files in repository
  * model_eval.ipynb: This notebook contains code for evaluating the performance of the trained models. It includes functions for data cleaning, preprocessing, model training, evaluation, and visualization.

### Software Setup
* Standard Python libraries (e.g., pandas, numpy, scikit-learn, matplotlib)
* Some other packages used: scipy, sklearn.preprocessing.

### Data
[Download the Kaggle dataset.](https://www.kaggle.com/competitions/playground-series-s3e26/data)

### Training
The 'fit' method is called, the model then learns the optimal parameters based on the training data

## Citations
* [Kaggle Challenge link.](https://www.kaggle.com/competitions/playground-series-s3e26/data)
