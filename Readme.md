# Weather Monitoring System

## Overview

The Weather Monitoring System is a Python application that fetches real-time weather data for a list of cities using the OpenWeatherMap API. It stores daily weather summaries in a SQLite database and checks for temperature thresholds to trigger alerts. The application also provides a simple visualization of temperature trends over time.

## Features

- Fetches real-time weather data for multiple cities.
- Stores daily weather summaries (average, maximum, minimum temperatures, and dominant weather condition) in a SQLite database.
- Checks for temperature breaches against a user-defined alert threshold.
- Visualizes temperature trends for each city using Matplotlib.

## Prerequisites

To run this application, you'll need the following:

- Python 3.x installed on your machine.
- Required Python packages:
  - `requests`
  - `sqlite3` (included with Python)
  - `matplotlib`

You can install the required packages using pip:

```bash
pip install requests matplotlib

API Key
You must obtain an API key from OpenWeatherMap and replace the existing API_KEY variable in the code with your own.

Usage
Clone the repository or download the code files.

Navigate to the project directory.

Open the terminal and run the application:

bash
Copy code
python weather_monitoring.py
When prompted, enter the temperature alert threshold in degrees Celsius.

The application will begin fetching weather data every 5 minutes and display alerts if any city's temperature exceeds the specified threshold. It will also save daily summaries to the SQLite database.

Database
The application uses SQLite to store daily weather summaries in a database named weather_data.db. The database contains the following table:

daily_weather_summary
Column	Type	Description
date	TEXT	The date of the weather data (YYYY-MM-DD).
city	TEXT	The name of the city.
avg_temp	REAL	The average temperature for the day (°C).
max_temp	REAL	The maximum temperature for the day (°C).
min_temp	REAL	The minimum temperature for the day (°C).
dominant_condition	TEXT	The most common weather condition.

Visualizations
The application generates a simple plot displaying temperature trends for each city over time. This visual representation helps users understand temperature fluctuations throughout the day.

Contributing
Feel free to contribute to this project by submitting issues or pull requests. Your feedback and improvements are welcome!