from your_module import GarchModel, SQLRepository
import sqlite3

# Create database connection
connection = sqlite3.connect('your_database.db')

# Initialize SQLRepository
sql_repo = SQLRepository(connection)

# Initialize GarchModel
model = GarchModel(ticker='AAPL', repo=sql_repo, use_new_data=True)

# Prepare data
model.wrangle_data(n_observations=1000)

# Fit model
model.fit(p=1, q=1)

# Predict volatility
forecasts = model.predict_volatility(horizon=5)
print(forecasts)

# Save model
filepath = model.dump()
print(f"Model saved to {filepath}")

# Load model
model.load()

