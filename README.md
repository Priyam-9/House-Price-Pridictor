House Price Predictor
![alt text](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat&logo=python)

![alt text](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-orange?style=flat&logo=scikit-learn)

![alt text](https://img.shields.io/badge/Pandas-Data_Processing-150458?style=flat&logo=pandas)

![alt text](https://img.shields.io/badge/NumPy-Numerical_Computing-013243?style=flat&logo=numpy)
An end-to-end Machine Learning regression project designed to predict real estate prices based on historical housing data. This project details the complete data science lifecycle: raw data ingestion, exploratory data analysis (EDA), feature engineering, multi-model evaluation (Linear Regression, SVR, Random Forest, XGBoost), and model serialization for real-time inference.
📋 Table of Contents
Overview & Workflow
Methodology (What We Did & How)
Tech Stack
Project Structure
Installation & Setup
Usage
🔍 Overview & Workflow
The primary objective of this project is to build a reliable regression model capable of predicting continuous housing prices. To achieve the best possible performance, multiple algorithms ranging from baseline parametric models to advanced tree-based ensembles were evaluated.
code
Text
Raw Data ➔ Data Cleaning & Scaling ➔ EDA & Feature Selection ➔ Multi-Model Training ➔ Evaluation (RMSE/R²) ➔ Serialization (.pkl)
🧠 Methodology (What We Did & How)
1. Data Cleaning & Preprocessing
Handling Missing Values: Applied statistical imputation (median/mean for continuous features, mode for categoricals) to resolve null values without heavily reducing dataset size.
Outlier Detection: Utilized Box plots and the Interquartile Range (IQR) method to cap or remove extreme outliers in continuous variables (e.g., heavily skewed income or room counts).
Feature Scaling: Applied StandardScaler / MinMaxScaler to normalize feature distributions, ensuring distance-based algorithms (like SVR) and gradient descent converge efficiently.
Categorical Encoding: Converted non-numeric features into machine-readable formats using One-Hot Encoding and Label Encoding.
2. Exploratory Data Analysis (EDA)
Correlation Analysis: Generated Seaborn heatmaps to identify multicollinearity between independent variables and find features with the highest correlation to the target price.
Distribution Checks: Plotted histograms and KDE plots to analyze skewness in the target variable (Price), applying log transformations where necessary to achieve normal distribution.
3. Model Training & Comparison
We trained and benchmarked four distinct regression models using Scikit-Learn and XGBoost libraries:
Linear Regression: Implemented as a baseline to establish linear relationships.
Support Vector Regression (SVR): Tested to capture complex non-linear boundary relationships using the RBF kernel.
Random Forest Regressor: A bagging ensemble method used to reduce variance and handle non-linear interactions without overfitting.
XGBoost Regressor: A robust gradient boosting framework that iteratively minimizes prediction errors, ultimately yielding the highest predictive accuracy.
Evaluation Metrics Used:
Mean Absolute Error (MAE)
Root Mean Squared Error (RMSE)
R
2
R 
2
 
 Score (Coefficient of Determination)
4. Model Deployment Preparation
The final top-performing model (based on validation 
R
2
R 
2
 
 score) was serialized using Pickle (house_price_model.pkl), decoupling the training logic from the inference engine.
Built an interactive entry point (app.py) allowing users to input custom housing parameters and receive real-time price estimations.
🛠️ Tech Stack
Core Language: Python 3.x
Data Processing & Manipulation: Pandas, NumPy
Machine Learning Frameworks: Scikit-Learn, XGBoost
Data Visualization: Matplotlib, Seaborn
Model Serialization: Pickle
📂 Project Structure
code
Text
House-Price-Predictor/
│
├── data/
│   └── housing.csv                 # Raw dataset
│
├── model/
│   └── house_price_model.pkl       # Serialized top-performing model
│
├── notebooks/
│   └── EDA_and_Model.ipynb         # Step-by-step EDA, preprocessing, & training logic
│
├── app.py                          # Application entry point for inference
├── requirements.txt                # Python package dependencies
└── README.md                       # Project documentation
⚙️ Installation & Setup
Follow these steps to set up the project locally.
Clone the repository:
code
Bash
git clone https://github.com/YOUR_USERNAME/House-Price-Predictor.git
cd House-Price-Predictor
Create a virtual environment (Recommended):
code
Bash
python -m venv venv
source venv/bin/activate      # On Windows use: venv\Scripts\activate
Install required dependencies:
code
Bash
pip install -r requirements.txt
🚀 Usage
Running Notebooks
To explore the complete data visualization and training workflow, launch Jupyter Notebook:
code
Bash
jupyter notebook notebooks/EDA_and_Model.ipynb
