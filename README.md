Predicting Air Quality Index (AQI) with Python
This project implements a machine learning pipeline to predict AQI levels using key pollutants like CO, Ozone, NO2, and PM2.5 from a geospatial dataset. It demonstrates end-to-end data science workflows suitable for data science students or early-career developers working on environmental ML projects.

Features
Data loading and preprocessing with Pandas and NumPy

Exploratory Data Analysis (EDA) using Matplotlib and Seaborn, including pair plots and correlation heatmaps

Train-test split (80/20) and model training with scikit-learn's RandomForestRegressor (MAE: ~0.09, R²: ~0.998)

Dataset
The dataset ("aqi_dataset.csv") includes columns for AQI Value, CO AQI Value, Ozone AQI Value, NO2 AQI Value, PM2.5 AQI Value, latitude, and longitude. The dataset will be provided separately for reproduction.

Requirements
```
pip install pandas numpy matplotlib seaborn scikit-learn
```
Run in Google Colab, Jupyter, or VS Code as the notebook is Colab-compatible.

Usage
Place "aqi_dataset.csv" in the working directory

Open Prdicting_AQI.ipynb and execute all cells sequentially

View EDA visualizations, train the model, and check metrics/plots for predictions vs. actual AQI

Model Performance
| Metric | Value |
|---|---|
| Mean Absolute Error | 0.089 |
| Mean Squared Error | 2.593 |
| R² Score | 0.998 |

The RandomForestRegressor excels due to handling non-linear pollutant-AQI relationships effectively.
