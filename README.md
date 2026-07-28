# Road Accident Analysis using Machine Learning

## Overview

This project analyzes historical road accident data from Delhi (2008–2017) using machine learning techniques. Two supervised learning tasks were performed using the same dataset:

- **Regression** – Predicting the expected number of injured people in a road accident.
- **Classification** – Predicting whether a road accident will result in one or more injuries.

The project demonstrates a complete machine learning workflow, including data cleaning, exploratory data analysis (EDA), feature engineering, preprocessing, model training, evaluation, and comparative analysis of multiple machine learning algorithms.

---

# Objectives

- Analyze historical road accident records from Delhi.
- Predict the expected number of injured people using regression models.
- Classify accidents as injury and non-injury cases using classification models.
- Compare multiple machine learning algorithms.
- Identify the best-performing model for each task.

---

# Dataset

The project uses the **Delhi Road Accident Dataset** containing accident records from **2008–2017**.

### Features

- YEAR
- DISTRICT
- VEHICLE AT FAULT
- VICTIM
- TYPE OF ACCIDENT

### Regression Target

- **# INJURED**

### Classification Target

A binary target variable was created from the **# INJURED** column.

| Target | Description |
|:------:|-------------|
| 0 | No injuries |
| 1 | One or more injuries |

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- CatBoost
- Imbalanced-Learn
- Joblib
- Jupyter Notebook

---

# Project Structure

```text
Accident-Prediction-Model/
│
├── data/
│   └── Delhi Accident Data.csv
│
├── notebooks/
│   ├── Accident_Regression.ipynb
│   └── Accident_Classification.ipynb
│
├── reports/
├── src/
├── requirements.txt
├── environment.yml
├── .gitignore
└── README.md
```

---

# Installation

Clone the repository.

```bash
git clone https://github.com/mjunaidk07/Accident-Prediction-Model.git
```

Move into the project directory.

```bash
cd Accident-Prediction-Model
```

Install the required dependencies.

```bash
pip install -r requirements.txt
```

---

# Usage

Launch Jupyter Notebook.

```bash
jupyter notebook
```

Navigate to the **notebooks** folder and open the notebook corresponding to the desired task.

### Regression Notebook

```
notebooks/Accident_Regression.ipynb
```

This notebook predicts the expected number of injured people using regression algorithms.

### Classification Notebook

```
notebooks/Accident_Classification.ipynb
```

This notebook predicts whether an accident will result in injuries using binary classification algorithms.

---

# Workflow

## Accident_Regression.ipynb

1. Load Dataset
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
5. Data Preprocessing
6. Train-Test Split
7. Train Regression Models
8. Evaluate Models
9. Compare Results

---

## Accident_Classification.ipynb

1. Load Dataset
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
5. Label Encoding
6. Train-Test Split
7. Train Classification Models
8. Evaluate Models
9. Compare Results

---

# Regression Models

- Linear Regression
- Decision Tree Regressor
- Linear Support Vector Regressor (LinearSVR)

---

# Classification Models

- Decision Tree Classifier
- AdaBoost Classifier
- Random Forest Classifier
- Linear Support Vector Classifier (LinearSVC)
- CatBoost Classifier
- Stacking Classifier

---

# Regression Evaluation Metrics

The regression models were evaluated using:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

---

# Classification Evaluation Metrics

The classification models were evaluated using:

- Accuracy
- Precision
- Recall
- F1 Score
- G-Mean
- Confusion Matrix
- Classification Report

---

# Results

## Regression Results

| Model | MAE | MSE | RMSE | R² Score |
|:------|----:|----:|-----:|---------:|
| Linear Regression | 0.3768 | 0.5991 | 0.7740 | 0.2388 |
| Decision Tree Regressor | **0.3448** | **0.5450** | **0.7382** | **0.3076** |
| LinearSVR | 0.2320 | 0.6475 | 0.8047 | 0.1772 |

**Best Regression Model:** Decision Tree Regressor

---

## Classification Results

| Model | Accuracy | F1 Score | G-Mean |
|:------|---------:|---------:|--------:|
| Decision Tree | **96.01%** | **97.37%** | **97.40%** |
| AdaBoost | **96.01%** | **97.37%** | **97.40%** |
| Random Forest | 95.25% | 96.91% | 94.92% |
| Linear SVC | 94.18% | 96.21% | 93.29% |
| CatBoost | 95.91% | 97.31% | 96.91% |
| Stacking Classifier | 95.91% | 97.31% | 96.86% |

**Best Classification Models:** Decision Tree Classifier and AdaBoost Classifier

---

# Discussion

The regression models were evaluated to estimate the number of injured people involved in road accidents. Among the evaluated models, the Decision Tree Regressor achieved the highest R² Score while maintaining the lowest prediction error, making it the best-performing regression model.

For the classification task, six different machine learning algorithms were compared. The Decision Tree Classifier and AdaBoost Classifier achieved the highest Accuracy, F1 Score, and G-Mean. Although CatBoost and the Stacking Classifier also demonstrated excellent performance, they did not outperform the simpler Decision Tree model. This suggests that the available features were sufficient for the Decision Tree to capture the underlying patterns in the dataset effectively.

---

# Conclusion

This project presents a comparative study of regression and classification techniques for road accident analysis using historical accident records from Delhi.

The regression notebook focuses on estimating the expected number of injured people, while the classification notebook predicts whether an accident will result in injuries.

The experiments demonstrate that:

- Decision Tree Regressor produced the best regression performance.
- Decision Tree Classifier and AdaBoost Classifier achieved the best classification performance with an Accuracy of **96.01%**, an F1 Score of **97.37%**, and a G-Mean of **97.40%**.
- More complex ensemble methods, including CatBoost and Stacking, produced competitive results but did not significantly improve performance over the Decision Tree model.

Overall, the project demonstrates an end-to-end supervised machine learning workflow, including data preprocessing, feature engineering, model training, evaluation, and comparative analysis.

---

# Future Improvements
- Develop a Streamlit web application for real-time predictions.
- Deploy the project as a REST API using Flask or FastAPI.

---

# Author

**Mohammad Junaid**

---
