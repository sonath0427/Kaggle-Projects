# Heart Disease Prediction – Kaggle Competition

## Overview

This project is a solution for the Kaggle Playground Series competition where the goal is to predict whether a patient has heart disease. The model is trained using the provided training dataset and generates predictions for the test dataset.

## Dataset

The dataset is provided by Kaggle and contains medical features related to patients.
The target variable is **Heart Disease**, which indicates whether the patient has heart disease.

Dataset files used:

* `train.csv`
* `test.csv`
* `sample_submission.csv`

Dataset source: Kaggle Playground Series.

## Approach

### 1. Data Preprocessing

* Loaded datasets using **pandas**
* Removed unnecessary columns (`id`)
* Separated features and target variable
* Converted categorical variables using **one-hot encoding**
* Aligned train and test datasets to ensure matching features

### 2. Train–Validation Split

The dataset was split into training and validation sets using an 80/20 split to evaluate model performance.

### 3. Model

Model used:

* Random Forest Classifier

Parameters:

* `n_estimators = 500`
* `random_state = 42`

### 4. Evaluation Metric

The model performance was evaluated using **ROC-AUC score** on the validation dataset.

### 5. Prediction

After training on the full dataset, predictions were generated for the test dataset and saved as `submission.csv`.

## Tools and Libraries

* Python
* pandas
* scikit-learn
* Google Colab

## Output

The final predictions were saved as:

`submission.csv`

This file can be uploaded directly to Kaggle for competition submission.

## Repository Structure

```
heart-disease-prediction/
│
├── Heart_Disease.ipynb
├── submission.csv
└── README.md
```

## Future Improvements

* Try Gradient Boosting models (XGBoost, LightGBM)
* Perform hyperparameter tuning
* Feature engineering to improve model performance
