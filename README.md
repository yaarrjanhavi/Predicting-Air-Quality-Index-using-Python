# Air Quality Index (AQI) Prediction with Machine Learning

A machine learning pipeline that predicts Air Quality Index levels using environmental pollutant data — including CO, Ozone, NO2, and PM2.5 — from a geospatial dataset. This project walks through a complete end-to-end data science workflow, making it an ideal reference for data science students and early-career developers exploring environmental ML applications.

---

## Features

- **Data Preprocessing** — Cleans and prepares raw data using Pandas and NumPy
- **Exploratory Data Analysis (EDA)** — Visualizes relationships between pollutants with pair plots and correlation heatmaps via Matplotlib and Seaborn
- **Model Training** — Trains a `RandomForestRegressor` using an 80/20 train-test split via scikit-learn
- **Evaluation** — Reports key regression metrics and generates prediction vs. actual AQI plots

---

## Dataset

The dataset (`aqi_dataset.csv`) contains the following columns:

| Column | Description |
|---|---|
| `AQI Value` | Target variable — overall air quality index |
| `CO AQI Value` | Carbon monoxide contribution |
| `Ozone AQI Value` | Ozone contribution |
| `NO2 AQI Value` | Nitrogen dioxide contribution |
| `PM2.5 AQI Value` | Fine particulate matter contribution |
| `latitude` | Geographic latitude |
| `longitude` | Geographic longitude |

> **Note:** The dataset must be provided separately and placed in the working directory before running the notebook.

---

## Requirements

Install the required Python libraries using:

```bash
pip install pandas numpy matplotlib seaborn scikit-learn
```

> Compatible with Google Colab, Jupyter Notebook, and VS Code.

---

## Usage

1. Place `aqi_dataset.csv` in your working directory
2. Open `Predicting_AQI.ipynb`
3. Run all cells sequentially to:
   - Preprocess the data
   - Explore and visualize pollutant distributions
   - Train the Random Forest model
   - Evaluate performance metrics and view prediction plots

---

## Model Performance

The `RandomForestRegressor` achieves near-perfect prediction accuracy by effectively capturing the non-linear relationships between pollutants and AQI.

| Metric | Value |
|---|---|
| Mean Absolute Error (MAE) | 0.089 |
| Mean Squared Error (MSE) | 2.593 |
| R² Score | 0.998 |

---

## Why Random Forest?

Random forests are well-suited for this task because pollutant-AQI relationships are inherently non-linear and multi-dimensional. The ensemble approach reduces overfitting while maintaining high predictive accuracy across varied geographic and environmental conditions.
