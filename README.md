# Stroke Prediction Machine Learning Model

## Project Overview

Stroke is one of the leading causes of death and disability worldwide. Early identification of patients at risk can help healthcare providers take preventative action and improve patient outcomes.

The goal of this project is to develop a machine learning model that predicts the likelihood of a stroke using patient demographic and health-related features.

Multiple classification models were trained and evaluated to determine the most suitable model for this prediction task.

---

## Dataset

The dataset contains patient demographic and medical information used to predict stroke occurrence.

### Features

- Age
- Gender
- Hypertension
- Heart disease
- Average glucose level
- Body Mass Index (BMI)
- Smoking status
- Marital status
- Work type
- Residence type

### Target Variable

stroke  
- **0** → No stroke  
- **1** → Stroke occurred

The dataset is imbalanced, with significantly fewer stroke cases than non-stroke cases.

---

## Project Workflow

The project followed a structured machine learning pipeline:

1. Data exploration and inspection
2. Data preprocessing
3. Feature encoding
4. Train/test split
5. Model training
6. Model evaluation
7. Prediction on unseen data

---

## Data Preprocessing

### Train/Test Split

The dataset was split into:

- **80% training data**
- **20% testing data**

Stratified sampling was used to maintain the class distribution.

### Encoding Categorical Variables

Several features in the dataset were categorical. These were converted into numerical format using **one-hot encoding** so they could be used by machine learning algorithms.

### Feature Alignment

After encoding, the training and testing datasets were aligned to ensure both contained identical feature columns.

---

## Models Used

Three machine learning models were trained and evaluated.

### Logistic Regression

A linear classification model commonly used for binary classification problems.

Class weighting was used to handle the class imbalance:
