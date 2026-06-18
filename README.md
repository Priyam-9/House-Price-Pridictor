# 🏠 House Price Predictor

An end-to-end **Machine Learning Regression Pipeline** designed to predict real estate prices using historical housing data. This project demonstrates the complete data science workflow — from **data preprocessing** and **exploratory data analysis (EDA)** to **feature engineering**, **multi-model evaluation**, and **model deployment preparation**.

The objective is to build a reliable regression system capable of accurately predicting continuous house prices based on multiple property-related features.

---

# 📋 Table of Contents

* [Overview](#-overview)
* [Workflow](#-workflow)
* [Methodology](#-methodology)
* [Tech Stack](#-tech-stack)
* [Project Structure](#-project-structure)
* [Installation & Setup](#-installation--setup)
* [Usage](#-usage)
* [Model Training](#-model-training)
* [Evaluation Metrics](#-evaluation-metrics)
* [Results](#-results)
* [Future Improvements](#-future-improvements)
* [Contributing](#-contributing)

---

# 🔍 Overview

House price prediction is a classic regression problem where the goal is to estimate the market price of a property based on features such as:

* Number of bedrooms
* Number of bathrooms
* Area (sq. ft.)
* Location
* Age of property
* Nearby amenities
* Other numerical/categorical variables

This project explores multiple regression models to identify the best-performing algorithm for real-world price estimation.

---

# ⚙ Workflow

```text
Raw Housing Data
        ↓
Data Cleaning & Preprocessing
        ↓
Exploratory Data Analysis (EDA)
        ↓
Feature Engineering & Scaling
        ↓
Train-Test Split
        ↓
Multi-Model Training
        ↓
Model Evaluation (RMSE, MAE, R²)
        ↓
Best Model Selection
        ↓
Model Serialization (.pkl)
```

This workflow ensures reproducibility, scalability, and structured model development.

---

# 🧠 Methodology

## 1. Data Ingestion

The housing dataset is loaded into Pandas DataFrames for preprocessing and analysis.

### Tasks performed:

* Import CSV dataset
* Inspect data types
* Check missing values
* Understand feature distributions

---

## 2. Data Cleaning

Raw data often contains inconsistencies.

### Cleaning steps:

✔ Handled missing values
✔ Removed duplicates
✔ Fixed inconsistent formats
✔ Dropped irrelevant columns

---

## 3. Exploratory Data Analysis (EDA)

EDA helps identify patterns, relationships, and anomalies.

### Analysis performed:

* Distribution plots
* Correlation heatmaps
* Outlier detection
* Feature-target relationships
* Skewness analysis

### Key insights:

* Strong correlation between area and price
* Location significantly impacts valuation
* Some features required transformation

---

## 4. Feature Engineering

Feature engineering improves model performance.

### Techniques used:

* Encoding categorical variables
* Feature scaling (StandardScaler)
* Log transformation (if required)
* Outlier treatment

---

## 5. Model Training

Multiple regression models were trained for comparison.

### Models used:

### 📈 Linear Regression

Baseline model for establishing initial performance.

### 🔄 Support Vector Regressor (SVR)

Useful for capturing non-linear relationships.

### 🌲 Random Forest Regressor

Ensemble learning model for improved accuracy and robustness.

### 🚀 XGBoost Regressor

Gradient boosting model optimized for high predictive performance.

---

## 6. Model Evaluation

Each model was evaluated using regression metrics.

Metrics used:

### RMSE (Root Mean Squared Error)

Measures average prediction error magnitude.

```math
RMSE = √(Σ(y - ŷ)² / n)
```

Lower RMSE = Better model.

---

### MAE (Mean Absolute Error)

```math
MAE = Σ|y - ŷ| / n
```

Measures average absolute difference.

---

### R² Score (Coefficient of Determination)

```math
R² = 1 - (SS_res / SS_tot)
```

Higher R² = Better explanatory power.

---

# 🛠 Tech Stack

## Programming Language

* Python

## Libraries

* Pandas
* NumPy
* Scikit-Learn
* Matplotlib
* Seaborn
* XGBoost
* Pickle

---

# 📂 Project Structure

```bash
House-Price-Predictor/
│── data/
│   ├── housing.csv
│
│── notebooks/
│   ├── eda.ipynb
│   ├── model_training.ipynb
│
│── models/
│   ├── linear_regression.pkl
│   ├── svr.pkl
│   ├── random_forest.pkl
│   ├── xgboost.pkl
│
│── src/
│   ├── preprocessing.py
│   ├── train.py
│   ├── evaluate.py
│
│── requirements.txt
│── README.md
```

---

# ⚡ Installation & Setup

## Clone the repository

```bash
git clone https://github.com/your-username/house-price-predictor.git
cd house-price-predictor
```

---

## Create virtual environment

```bash
python -m venv venv
```

Activate it:

### Windows

```bash
venv\Scripts\activate
```

### Mac/Linux

```bash
source venv/bin/activate
```

---

## Install dependencies

```bash
pip install -r requirements.txt
```

---

# ▶ Usage

Run model training:

```bash
python src/train.py
```

Run evaluation:

```bash
python src/evaluate.py
```

Load saved model:

```python
import pickle

model = pickle.load(open("models/xgboost.pkl", "rb"))

prediction = model.predict([[3, 2, 1500, 5]])
print(prediction)
```

---

# 📊 Model Training Summary

| Model             | Strength                    |
| ----------------- | --------------------------- |
| Linear Regression | Simple baseline             |
| SVR               | Non-linear pattern learning |
| Random Forest     | Handles complexity well     |
| XGBoost           | High-performance boosting   |

---

# 📈 Results

After evaluation:

✅ XGBoost achieved the best performance
✅ Random Forest showed strong robustness
✅ Linear Regression provided interpretability
✅ SVR captured non-linear behavior effectively

Final selected model was serialized for deployment.

Example:

```bash
models/best_model.pkl
```

---

# 🚀 Future Improvements

* Hyperparameter tuning with GridSearchCV
* Deploy using Flask/FastAPI
* Add Streamlit frontend
* Integrate live property data APIs
* Model monitoring and retraining pipeline

---

# 🤝 Contributing

Contributions are welcome.

Steps:

1. Fork the repository
2. Create a new branch
3. Commit changes
4. Push the branch
5. Open a Pull Request

---

# 📜 License

This project is licensed under the MIT License.

---

# 👨‍💻 Author

**Priyam Patel**
Data Analyst Intern @ TV9
Machine Learning | Data Engineering | Business Analytics
