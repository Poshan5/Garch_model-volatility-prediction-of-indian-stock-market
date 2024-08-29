# AlphaVantage API and SQLite Integration

This project includes code for interacting with the AlphaVantage API to fetch historical stock data and storing this data in an SQLite database. The API key required for AlphaVantage is securely stored in a `.env` file and imported via the `config` module.

## Overview

This project provides two main classes:

1. **AlphaVantageAPI**: 
   - Fetches daily time series data for a given ticker symbol from the AlphaVantage API.
   - Returns the data as a pandas DataFrame.

2. **SQLRepository**: 
   - Handles interactions with an SQLite database.
   - Provides methods to insert data into a table and read data from a table.

## Features

- **AlphaVantageAPI**:
  - `get_daily(ticker, output_size="full")`: Retrieves daily stock data for a specified ticker symbol.
  
- **SQLRepository**:
  - `insert_table(table_name, records, if_exists)`: Inserts a pandas DataFrame into a specified SQLite table.
  - `read_table(table_name, limit=None)`: Reads data from a specified SQLite table into a pandas DataFrame.

## Requirements

Ensure you have Python 3.x installed and the following packages:

- pandas
- requests
- sqlite3

Install the required packages using `pip`:

```bash
pip install pandas requests
