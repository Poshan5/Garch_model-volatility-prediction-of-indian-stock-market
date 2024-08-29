# GARCH Model for Volatility Prediction

This project features a Python class for training and using a GARCH (Generalized Autoregressive Conditional Heteroskedasticity) model to forecast market volatility. The `GarchModel` class integrates with the AlphaVantage API to fetch stock data and uses SQLite for data management. It also includes functionality to save and load models using joblib.

## Overview

The `GarchModel` class provides functionalities to:

- Fetch and preprocess historical stock data.
- Train a GARCH model on the data.
- Forecast future volatility.
- Save and load trained models.

## Features

- **Data Handling**:
  - Fetch new data from AlphaVantage or use existing data stored in an SQLite database.
  - Transform and prepare data for training.

- **Model Training**:
  - Train a GARCH model with specified parameters.
  - Calculate model selection criteria (AIC and BIC).

- **Prediction**:
  - Generate and format volatility forecasts for a specified horizon.

- **Model Persistence**:
  - Save the trained model to disk.
  - Load the most recent model from disk.

## Requirements

Ensure you have Python 3.x installed and the following packages:

- `pandas`
- `numpy`
- `scipy`
- `arch`
- `joblib`
- `requests`
- `sqlite3`

Install the required packages using `pip`:

```bash
pip install pandas numpy scipy arch joblib requests
