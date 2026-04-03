# 🧠 Stroke Prediction Machine Learning Model

## 📌 Project Overview

Stroke is one of the leading causes of death and long-term disability worldwide. Early identification of high-risk individuals can support preventative care and reduce adverse outcomes.

This project aims to build a machine learning model that predicts the likelihood of a stroke based on patient demographic and health-related data.

Multiple classification models were developed and evaluated to identify the most effective approach for this imbalanced classification problem.

---

## 📊 Dataset

The dataset includes patient-level health and demographic information.

### Features

- Age  
- Gender  
- Hypertension (0/1)  
- Heart Disease (0/1)  
- Average Glucose Level  
- Body Mass Index (BMI)  
- Smoking Status  
- Marital Status  
- Work Type  
- Residence Type  

### Target Variable

- **Stroke**
  - `0` → No stroke  
  - `1` → Stroke occurred  

⚠️ **Note:** The dataset is highly imbalanced, with significantly fewer stroke cases than non-stroke cases. This impacts model performance and evaluation strategy.

---

## 🔄 Project Workflow

The project follows a structured machine learning pipeline:

1. Data exploration and inspection  
2. Data cleaning and preprocessing  
3. Feature encoding  
4. Train/test split (stratified)  
5. Model training  
6. Model evaluation  
7. Prediction on unseen data  

---

## 🧹 Data Preprocessing

### Train/Test Split

- 80% training data  
- 20% testing data  
- **Stratified sampling** used to preserve class distribution  

### Handling Categorical Variables

- Applied **one-hot encoding** to convert categorical variables into numerical format  

### Feature Alignment

- Ensured training and testing datasets had identical feature columns after encoding  

### Missing Values

- BMI contained missing values  
- These were handled using **imputation (e.g., mean/median)**  

---

## Models Used
### 1. Logistic Regression
Baseline model for binary classification.

Applied class weighting (class_weight='balanced') to address the significant class imbalance.

### 2. Decision Tree Classifier
Used to capture non-linear decision boundaries within the health metrics.

Provides high interpretability for clinical risk factors.

### 3. Random Forest Classifier
An ensemble method used to improve accuracy and reduce the risk of overfitting inherent in single decision trees.

Processes multiple decision trees to produce a more robust prediction.

---

## 📈 Model Evaluation

Due to class imbalance, accuracy alone is not a reliable metric.

### Metrics Used

- Precision  
- Recall  
- F1 Score  
- ROC-AUC  

### Key Focus

- **Recall for stroke cases (class = 1)**  
  → Important to minimise false negatives (i.e., missed stroke risks)

---

## ⚠️ Current Limitations

- Imbalanced dataset may bias predictions toward non-stroke cases  
- Limited feature set (no lifestyle or longitudinal health data)  
- No hyperparameter tuning fully completed  
- Model interpretability not deeply explored yet  

---

## 🚧 Work in Progress / Next Steps

This project is still being improved. Planned enhancements include:

- 🔹 Hyperparameter tuning (GridSearch / RandomSearch)  
- 🔹 Advanced imbalance handling (SMOTE, undersampling)  
- 🔹 Feature importance analysis  
- 🔹 Model explainability (e.g., SHAP values)  
- 🔹 Deployment (Streamlit or Flask app)  

---

## 💡 Key Learnings

- Handling imbalanced datasets in real-world problems  
- Importance of choosing the right evaluation metrics  
- End-to-end machine learning workflow  
- Data preprocessing and feature engineering for tabular data  

---

## 🛠️ Tech Stack

- Python  
- Pandas  
- NumPy  
- Scikit-learn  
- Matplotlib / Seaborn  

---

## 📎 Project Status

🚧 **In Progress** – Core modelling complete, currently improving performance and interpretability.

---

## 👤 Author

**Emmanuel Oloruntola**  
Aspiring Data Analyst / Data Scientist  
