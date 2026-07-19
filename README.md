# Accident Prediction Model

## Overview

This project predicts the expected number of injured people in a road accident using machine learning techniques. The model is trained on the Delhi Accident Dataset and learns patterns from historical accident records.

## Features

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Linear Regression
- Decision Tree Regression
- Support Vector Regression (SVR)
- Model Evaluation
- Prediction on New Data

## Dataset

The dataset contains historical road accident records from Delhi (2007–2017).

### Features Used

- YEAR
- DISTRICT
- VEHICLE AT FAULT
- VICTIM
- TYPE OF ACCIDENT

### Target Variable

- # INJURED

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

## Project Structure

```
Accident-Prediction-Model/
│
├── data/
│   └── Delhi Accident Data.csv
├── notebooks/
│   └── Accident_Prediction.ipynb
├── models/
├── requirements.txt
├── environment.yml
└── README.md
```

## Workflow

1. Load Dataset
2. Data Cleaning
3. Exploratory Data Analysis
4. Feature Engineering
5. Train Machine Learning Models
6. Evaluate Models
7. Compare Performance
8. Predict Number of Injured People

## Models Used

- Linear Regression
- Decision Tree Regression
- Support Vector Regression (SVR)

## Evaluation Metrics

- Mean Absolute Error (MAE)
- Mean Squared Error (MSE)
- Root Mean Squared Error (RMSE)
- R² Score

## Results

The performance of the machine learning models was evaluated using Mean Absolute Error (MAE), Mean Squared Error (MSE), Root Mean Squared Error (RMSE), and R² Score.

| Model | MAE | MSE | RMSE | R² Score |
|:------|----:|----:|-----:|---------:|
| Linear Regression | 0.3768 | 0.5991 | 0.7740 | 0.2388 |
| Decision Tree Regression (`max_depth=5`) | 0.3448 | 0.5450 | 0.7382 | 0.3076 |
| Support Vector Regression (SVR) | - | - | - | - |

**Current Best Model:** Decision Tree Regression (`max_depth=5`)

The tuned Decision Tree Regression model achieved the best performance among the evaluated models so far. Limiting the tree depth to 5 reduced overfitting and improved prediction accuracy, resulting in lower error values and a higher R² score than the Linear Regression model.

## Conclusion

The models were trained on historical accident data to estimate the expected number of injured people based on accident characteristics. Their performance was compared using standard regression metrics, and the best-performing model was selected for prediction.

## Future Improvements

- Add weather information
- Include time of day
- Include road condition
- Add traffic density
- Deploy the model using Flask or Streamlit

## Author

Mohammad Junaid