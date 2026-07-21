# Accident Prediction Model

## Overview

This project predicts the expected number of injured people in road accidents using machine learning techniques. The model is trained on the Delhi Accident Dataset and learns patterns from historical accident records to estimate the number of injuries based on accident characteristics.

---

## Features

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Data Preprocessing
- Linear Regression
- Decision Tree Regression
- Linear Support Vector Regression (LinearSVR)
- Model Evaluation
- Model Comparison
- Prediction on New Data

---

## Dataset

The dataset contains historical road accident records from Delhi covering the years **2007–2017**.

### Features Used

- YEAR
- DISTRICT
- VEHICLE AT FAULT
- VICTIM
- TYPE OF ACCIDENT

### Target Variable

- # INJURED

---

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

---

## Project Structure

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

## Installation

Clone the repository:

```bash
git clone https://github.com/mjunaidk07/Accident-Prediction-Model.git
```

Move into the project directory:

```bash
cd Accident-Prediction-Model
```

Install the required packages:

```bash
pip install -r requirements.txt
```

---

## Usage

Open the notebook:

```bash
jupyter notebook
```

Navigate to:

```
notebooks/Accident_Prediction.ipynb
```

Run the notebook cells sequentially to reproduce the results.

---

## Workflow

1. Load Dataset
2. Data Cleaning
3. Exploratory Data Analysis (EDA)
4. Feature Engineering
5. Label Encoding
6. Feature Scaling
7. Train-Test Split
8. Train Machine Learning Models
9. Evaluate Models
10. Compare Model Performance
11. Save the Best Model

---

## Machine Learning Models

- Linear Regression
- Decision Tree Regression
- Linear Support Vector Regression (LinearSVR)

---

## Evaluation Metrics

The models are evaluated using the following regression metrics:

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

---

## Results

| Model | MAE | MSE | RMSE | R² Score |
|:------|----:|----:|-----:|---------:|
| Linear Regression | 0.3768 | 0.5991 | 0.7740 | 0.2388 |
| Decision Tree Regression (`max_depth=5`) | **0.3448** | **0.5450** | **0.7382** | **0.3076** |
| LinearSVR | 0.2320 | 0.6475 | 0.8047 | 0.1772 |

---

## Best Performing Model

**Decision Tree Regression (`max_depth=5`)**

The Decision Tree Regression model achieved the highest R² Score and the lowest RMSE among the evaluated models. Limiting the tree depth to **5** reduced overfitting and improved generalization, making it the best-performing model for this dataset.

---

## Saved Models

The following files are generated after training:

- `decision_tree_model.pkl` – Trained Decision Tree model
- `scaler.pkl` – StandardScaler used for feature scaling
- `label_encoders.pkl` – Label encoders for categorical features

These files can be loaded later without retraining the model.

---

## Conclusion

Historical road accident data was analyzed and multiple regression models were trained to estimate the expected number of injured people.

Among the evaluated models, **Decision Tree Regression** provided the best overall predictive performance and was selected as the final model. The project demonstrates the complete machine learning workflow, including data preprocessing, feature engineering, model training, evaluation, comparison, and model serialization for future deployment.

---

## Future Improvements

- Develop a Streamlit web application for predictions
- Perform hyperparameter tuning
- Train on a larger and more recent dataset
- Incorporate additional features such as weather conditions, road conditions, and traffic density
- Deploy the application to the cloud

---

## Author

**Mohammad Junaid**

---

## License

This project is intended for educational purposes.