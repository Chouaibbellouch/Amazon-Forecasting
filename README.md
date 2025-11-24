# Amazon Forecasting

Time series forecasting project for electricity price prediction using machine learning models.

## Overview

This project implements electricity price forecasting using advanced machine learning techniques. The project uses historical electricity price data from the AutoGluon dataset to train and evaluate predictive models.

## Features

- **Multiple ML Models**: Implementation of XGBoost and LightGBM regressors
- **Hyperparameter Optimization**: Automated hyperparameter tuning using Hyperopt
- **Time Series Cross-Validation**: Proper time series split for model validation
- **Experiment Tracking**: MLflow integration for tracking experiments and model versioning
- **Visualization**: Comprehensive plots comparing model predictions against actual values

## Technologies Used

- **Python**: Primary programming language
- **Pandas**: Data manipulation and analysis
- **XGBoost**: Gradient boosting framework
- **LightGBM**: Light gradient boosting machine
- **Hyperopt**: Hyperparameter optimization library
- **MLflow**: Experiment tracking and model registry
- **Matplotlib**: Data visualization
- **scikit-learn**: Machine learning utilities and metrics

## Dataset

The project uses the electricity price dataset from AutoGluon:
- **Source**: `https://autogluon.s3.amazonaws.com/datasets/timeseries/electricity_price/train.parquet`
- **Features**:
  - `id`: Region identifier (DE - Germany)
  - `timestamp`: Time of the observation
  - `target`: Electricity price (target variable)
  - `Ampirion Load Forecast`: Load forecast data (from Amprion TSO)
  - `PV+Wind Forecast`: Photovoltaic and wind generation forecast

## Installation

1. Clone the repository:
```bash
git clone https://github.com/Chouaibbellouch/Amazon-Forecasting.git
cd Amazon-Forecasting
```

2. Install required dependencies:
```bash
pip install pandas matplotlib mlflow hyperopt xgboost lightgbm scikit-learn
```

## Usage

Open and run the Jupyter notebook:
```bash
jupyter notebook amazon.ipynb
```

The notebook includes the following steps:
1. Data loading and exploration
2. Data preprocessing and feature engineering
3. Model training with hyperparameter optimization
4. Model evaluation using time series cross-validation
5. Model registration with MLflow
6. Predictions and visualization

## Project Structure

```
Amazon-Forecasting/
├── amazon.ipynb         # Main Jupyter notebook with the complete pipeline
├── .gitignore          # Git ignore configuration
└── README.md           # Project documentation
```

## Model Performance

The project implements two models:
- **XGBoost**: With optimized hyperparameters for time series forecasting
- **LightGBM**: With optimized hyperparameters for efficient training

Both models are evaluated using:
- Root Mean Squared Error (RMSE)
- Mean Absolute Error (MAE)
- R² Score

## MLflow Tracking

The project uses MLflow for:
- Logging hyperparameters and metrics
- Model versioning
- Model registry (production models)
- Experiment comparison

## License

This project is available for educational and research purposes.

## Author

Chouaib Bellouch
