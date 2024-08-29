# GARCH Model for Volatility Prediction

This project includes a Python class for training a GARCH (Generalized Autoregressive Conditional Heteroskedasticity) model to predict market volatility. The `GarchModel` class interacts with both the AlphaVantage API to fetch stock data and an SQLite database to store and retrieve data. It also provides functionality to save and load trained models using joblib.

## Overview

The `GarchModel` class provides methods for:

- Fetching and preprocessing historical stock data.
- Training a GARCH model on the data.
- Predicting future volatility.
- Saving and loading trained models.

## Features

- **Data Handling**:
  - Fetch new data from AlphaVantage or use existing data from an SQLite database.
  - Process and prepare data for training.

- **Model Training**:
  - Train a GARCH model with specified parameters.
  - Compute and report model selection criteria (AIC and BIC).

- **Prediction**:
  - Generate volatility forecasts for a given forecast horizon.
  - Format predictions for easy use.

- **Model Persistence**:
  - Save trained models to disk.
  - Load the most recent model from disk.

## Requirements

Ensure you have Python 3.x installed and the following packages:

- pandas
- numpy
- scipy
- arch
- joblib
- requests
- sqlite3

Install the required packages using `pip`:

```bash
pip install pandas numpy scipy arch joblib requests
