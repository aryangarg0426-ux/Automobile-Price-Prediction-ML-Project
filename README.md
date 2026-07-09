# Automobile-Price-Prediction-ML-Project

An end-to-end Data Science and Machine Learning project that analyzes used car market data and predicts selling prices using Exploratory Data Analysis (EDA) and regression algorithms.

---

## 📌 Table of Contents
- [Project Overview](#-project-overview)
- [Key Features](#-key-features)
- [Dataset Information](#-dataset-information)
- [Project Workflow](#-project-workflow)
- [Machine Learning Models & Evaluation](#-machine-learning-models--evaluation)
- [Technologies & Libraries Used](#-technologies--libraries-used)
- [Installation & Setup](#-installation--setup)
- [Usage Guide](#-usage-guide)
- [Project Structure](#-project-structure)
- [Future Improvements](#-future-improvements)

---

## 🏎️ Project Overview

Valuing used cars accurately is a challenging problem in the automotive industry due to multi-dimensional factors such as vehicle age, mileage driven, brand reputation, engine capacity, fuel type, and ownership history. 

This project aims to:
1. Conduct an in-depth **Exploratory Data Analysis (EDA)** to discover key market trends and price drivers.
2. Clean and preprocess complex text and categorical vehicle specifications.
3. Train, evaluate, and compare multiple **Machine Learning Regression Models** (Linear Regression, Random Forest, and XGBoost) to accurately estimate used car selling prices.

---

## ✨ Key Features

- **Data Cleaning & Wrangling**: Handles missing values, strips string units (e.g., `kmpl`, `CC`, `bhp`), and parses vehicle attributes.
- **Brand Feature Extraction**: Extracts brand names from full vehicle title strings to analyze manufacturer market distribution.
- **Visual Exploratory Data Analysis**: Visualizes market trends, including brand frequency distributions, feature correlations, and price distributions using Seaborn & Matplotlib.
- **Categorical Encoding**: Implements `LabelEncoder` and `OrdinalEncoder` for categorical variables such as fuel type, seller type, transmission, and owner count.
- **Model Benchmarking**: Trains and compares multiple algorithms with cross-validation and evaluation metrics ($R^2$ Score, MSE/RMSE).

---

## 📊 Dataset Information

The model is trained on the **Car Details v3** dataset (`Car details v3.csv`), containing detailed specifications of used cars.

- **Initial Dataset Size**: 8,128 records × 13 attributes
- **Cleaned Dataset Size**: 7,906 records (after removing null values)

### Attribute Details

| Column Name | Data Type | Description |
| :--- | :--- | :--- |
| `name` | Object | Full vehicle name (brand, model, variant) |
| `year` | Integer | Year of vehicle manufacture |
| `selling_price` | Integer | **Target Variable**: Vehicle selling price (in INR) |
| `km_driven` | Integer | Total kilometers driven by the vehicle |
| `fuel` | Object | Fuel type (`Petrol`, `Diesel`, `CNG`, `LPG`) |
| `seller_type` | Object | Type of seller (`Individual`, `Dealer`, `Trustmark Dealer`) |
| `transmission` | Object | Gearbox type (`Manual`, `Automatic`) |
| `owner` | Object | Ownership count (`First Owner`, `Second Owner`, etc.) |
| `mileage` | Object / Float | Fuel efficiency (e.g., `20.36 kmpl`) |
| `engine` | Object / Float | Engine capacity in CC (e.g., `1197 CC`) |
| `max_power` | Object / Float | Maximum engine power in bhp (e.g., `78.9 bhp`) |
| `torque` | Object | Engine torque specifications |
| `seats` | Float | Seating capacity |

---

## 🔄 Project Workflow
