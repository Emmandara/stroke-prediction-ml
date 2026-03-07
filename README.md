# stroke-prediction-ml
Stroke Prediction Machine Learning Model
Project Overview

Stroke is one of the leading causes of death and disability worldwide. Early identification of patients at risk can help healthcare providers take preventative action and improve patient outcomes.

The aim of this project is to build a machine learning model that predicts the likelihood of a stroke based on patient demographic and health-related features.

Multiple classification models were trained and evaluated to determine the most suitable model for this prediction task.

Dataset

The dataset contains patient demographic and medical information used to predict stroke occurrence.

Features include

Age

Gender

Hypertension

Heart disease

Average glucose level

Body Mass Index (BMI)

Smoking status

Marital status

Work type

Residence type

Target Variable
stroke

0 → No stroke

1 → Stroke occurred

The dataset is imbalanced, with significantly fewer stroke cases than non-stroke cases.

Project Workflow

The project followed a standard machine learning pipeline:

Data exploration and inspection

Data preprocessing

Feature encoding

Train/test split

Model training

Model evaluation

Prediction on unseen data

Data Preprocessing
Train-Test Split

The dataset was split into:

80% training data

20% testing data

Stratified sampling was used to preserve the class distribution.

Encoding Categorical Variables

Several features were categorical (text values). These were converted into numerical format using one-hot encoding so they could be used in machine learning models.

Feature Alignment

After encoding, the training and testing datasets were aligned to ensure they contained identical feature columns. This prevents errors during model prediction.

Models Used

Three classification algorithms were trained and evaluated.

Logistic Regression

A linear classification model commonly used for binary classification problems.

Class weighting was used to address the imbalanced dataset:

class_weight = "balanced"

This allows the model to pay more attention to the minority class (stroke cases).

Decision Tree Classifier

A non-linear model that splits data into branches based on feature values. Decision Trees can capture complex relationships within the dataset.

Random Forest Classifier

An ensemble learning method that combines multiple decision trees to improve predictive performance and reduce overfitting.

Model Evaluation

The models were evaluated using standard classification metrics:

Precision

Recall

F1-score

Confusion Matrix

For medical prediction tasks, recall is particularly important. High recall ensures that most stroke cases are correctly identified, reducing the risk of false negatives.

False negatives are especially dangerous in healthcare because patients at risk may not receive necessary medical attention.

Final Model Selection

After evaluating the models, Logistic Regression was selected as the final model.

The model achieved balanced performance and strong recall when predicting stroke cases, making it suitable for identifying high-risk patients.

Prediction on Unseen Data

The final model was applied to a separate unseen dataset to simulate real-world predictions.

The unseen dataset was processed using the same preprocessing steps:

categorical encoding

feature alignment

Predictions were generated using the trained Logistic Regression model and exported to a CSV file.

Technologies Used

Python libraries used in this project include:

pandas

numpy

scikit-learn

matplotlib

Machine learning models used:

Logistic Regression

Decision Tree Classifier

Random Forest Classifier

Project Structure
stroke-prediction-project
│
├── Stroke_Prediction_EDA.ipynb
├── brain_stroke.csv
├── brain_stroke_unseen.csv
├── predictions.csv
└── README.md
Key Skills Demonstrated

Data exploration and analysis

Data preprocessing

Handling categorical variables

Addressing class imbalance

Machine learning model training

Model evaluation and comparison

Generating predictions on unseen data

Future Improvements

Possible improvements include:

Hyperparameter tuning

Cross-validation

Feature importance analysis

Testing additional algorithms such as Gradient Boosting
