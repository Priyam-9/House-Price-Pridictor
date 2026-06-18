# House Price Predictor

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?style=flat&logo=python)](https://www.python.org/)
[![Scikit-Learn](https://img.shields.io/badge/Scikit--Learn-Machine_Learning-orange?style=flat&logo=scikit-learn)](https://scikit-learn.org/)
[![Pandas](https://img.shields.io/badge/Pandas-Data_Processing-150458?style=flat&logo=pandas)](https://pandas.pydata.org/)
[![NumPy](https://img.shields.io/badge/NumPy-Numerical_Computing-013243?style=flat&logo=numpy)](https://numpy.org/)

An end-to-end Machine Learning regression project designed to predict real estate prices based on historical housing data. This project covers the primary stages of the data science lifecycle: data ingestion, exploratory data analysis (EDA), feature engineering, multi-model evaluation (**Linear Regression, SVR, Random Forest, XGBoost**), and model serialization for inference.

---

## 📋 Table of Contents
- [Overview & Workflow](#-overview--workflow)
- [Methodology (What We Did & How)](#-methodology-what-we-did--how)
- [Tech Stack](#-tech-stack)
- [Project Structure](#-project-structure)
- [Installation & Setup](#-installation--setup)
- [Usage](#-usage)

---

## 🔍 Overview & Workflow

The primary objective of this project is to build a reliable regression model capable of predicting continuous housing prices. To achieve this, multiple algorithms—ranging from baseline parametric models to advanced tree-based ensembles—were trained, evaluated, and compared.

```text
Raw Data ➔ Data Cleaning & Scaling ➔ EDA & Feature Selection ➔ Multi-Model Training ➔ Evaluation (RMSE/R²) ➔ Serialization (.pkl)
