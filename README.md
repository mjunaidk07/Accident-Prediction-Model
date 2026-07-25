# Road Accident Analysis using Machine Learning

## Overview

This project applies machine learning techniques to analyze historical road accident data from Delhi (2007–2017). Two predictive tasks were performed using the same dataset:

- **Regression:** Predict the expected number of injured people in a road accident.
- **Classification:** Predict whether a road accident will result in one or more injuries.

The project demonstrates the complete machine learning pipeline, including data cleaning, exploratory data analysis, feature engineering, preprocessing, model training, evaluation, comparison, and model serialization.

---

# Objectives

- Analyze historical road accident data.
- Predict the expected number of injured persons using regression models.
- Classify accidents as injury or non-injury cases using classification models.
- Compare multiple machine learning algorithms.
- Identify the best-performing models for both prediction tasks.

---

# Dataset

The dataset contains historical road accident records from **Delhi (2007–2017)**.

### Features

- YEAR
- DISTRICT
- VEHICLE AT FAULT
- VICTIM
- TYPE OF ACCIDENT

### Regression Target

- **# INJURED**

### Classification Target

A binary target variable was created:

| Value | Meaning |
|------:|---------|
| 0 | No injuries |
| 1 | One or more injuries |

Generated using:

```python
TARGET = (# INJURED > 0)
```

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

```
Accident-Prediction-Model/
│
├── data/
│   └── Delhi Accident Data.csv
│
├── models/
│   ├── decision_tree_model.pkl
│   ├── scaler.pkl
│   └── label_encoders.pkl
│
├── notebooks/
│   └── Accident_Prediction.ipynb
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

Navigate to the project folder.

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

Open

```
notebooks/Accident_Prediction.ipynb
```

Run all notebook cells sequentially.

---

# Workflow

1. Load Dataset
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
5. Data Preprocessing
6. Label Encoding
7. Train-Test Split
8. Train Regression Models
9. Train Classification Models
10. Evaluate Models
11. Compare Results
12. Save the Best Model

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

# Regression Results

| Model | MAE | MSE | RMSE | R² Score |
|:------|----:|----:|-----:|---------:|
| Linear Regression | 0.3768 | 0.5991 | 0.7740 | 0.2388 |
| Decision Tree Regressor | **0.3448** | **0.5450** | **0.7382** | **0.3076** |
| LinearSVR | 0.2320 | 0.6475 | 0.8047 | 0.1772 |

---

# Classification Results

| Model | Accuracy | F1 Score | G-Mean |
|:------|---------:|---------:|--------:|
| Decision Tree | **96.01%** | **97.37%** | **97.40%** |
| AdaBoost | **96.01%** | **97.37%** | **97.40%** |
| Random Forest | 95.25% | 96.91% | 94.92% |
| Linear SVC | 94.18% | 96.21% | 93.29% |
| CatBoost | 95.91% | 97.31% | 96.91% |
| Stacking Classifier | 95.91% | 97.31% | 96.86% |

---

# Best Performing Models

## Regression

**Decision Tree Regressor (max_depth = 5)**

The Decision Tree Regressor achieved the best regression performance by obtaining the highest R² Score while maintaining the lowest RMSE among the evaluated regression models.

---

## Classification

**Decision Tree Classifier (max_depth = 5)**

The Decision Tree Classifier achieved the best overall classification performance with:

- Accuracy: **96.01%**
- F1 Score: **97.37%**
- G-Mean: **97.40%**

AdaBoost achieved identical performance, while CatBoost and the Stacking Classifier produced comparable results but did not surpass the Decision Tree.

---



# Conclusion

This project explored both **regression** and **classification** techniques for analyzing road accident data.

For the regression task, three machine learning models were trained to estimate the expected number of injured people. Among them, the Decision Tree Regressor achieved the best predictive performance.

For the classification task, six machine learning algorithms were evaluated to predict whether an accident would result in injuries. The Decision Tree Classifier and AdaBoost Classifier achieved the highest performance, with an accuracy of **96.01%**, an F1 Score of **97.37%**, and a G-Mean of **97.40%**. Although advanced ensemble methods such as CatBoost and Stacking Classifier delivered excellent results, they did not outperform the simpler Decision Tree model on this dataset.

Overall, the project demonstrates an end-to-end machine learning workflow, including data preprocessing, feature engineering, model training, evaluation, comparison, and model serialization.

---

# Future Improvements

- Train using larger and more recent datasets
- Develop a Streamlit web application for real-time predictions
- Deploy the trained model using Flask/FastAPI on a cloud platform

---

# Author

**Mohammad Junaid**

---

# License

This project is intended for educational and research purposes.