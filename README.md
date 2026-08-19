# Weather Data ETL Pipeline

## Project Overview

This project demonstrates a basic ETL (Extract, Transform, Load) pipeline using real-time weather data from the OpenWeather API.

The pipeline extracts weather data for five Nigerian cities, transforms the data into a clean and structured format using Python and Pandas, stores the processed data as a CSV file, and performs basic analysis to generate insights.

## Objective

The objective of this project is to understand and demonstrate how an ETL pipeline can be used to collect data from an API, transform it into a usable format, store it for future analysis, and generate meaningful insights.

## Data Source

**OpenWeather API**

Weather data was collected from the OpenWeather Current Weather API.

The cities analyzed were:

- Lagos
- Abuja
- Kaduna
- Kano
- Maiduguri

The following weather information was collected:

- City Name
- Temperature
- Humidity
- Weather Condition
- Wind Speed
- Date and Time

## ETL Process

### 1. Extract

The weather data was extracted from the OpenWeather API using Python and the `Requests` library.

A Python function was created to send API requests for each city and retrieve the required weather information.

Five Nigerian cities were used, exceeding the minimum requirement of three cities.

### 2. Transform

The extracted JSON data was converted into a Pandas DataFrame.

The transformation process included:

- Structuring the API response into tabular data
- Using meaningful column names
- Converting Unix timestamps into readable date and time values
- Removing the unnecessary raw timestamp column
- Checking for missing values
- Checking for duplicate records
- Verifying appropriate data types

The final dataset contained **0 missing values** and **0 duplicate records**.

### 3. Load

The transformed dataset was saved as a CSV file:

`data/processed_weather_data.csv`

This allows the processed data to be used for future analysis without requiring another API request.

## Tools and Technologies

- Python
- Pandas
- Requests
- Matplotlib
- Python-dotenv
- OpenWeather API
- Jupyter Notebook
- VS Code
- Git
- GitHub

## Basic Analysis

The processed weather data was analyzed to compare temperature, humidity, wind speed, and weather conditions across the five cities.

### Key Findings

- The average temperature across the five cities was **26.85°C**.
- The average humidity was **74.8%**.
- The average wind speed was **2.54 m/s**.
- **Maiduguri** recorded the highest temperature at **32.39°C**.
- **Abuja** recorded the lowest temperature at **23.60°C**.
- **Abuja** recorded the highest humidity at **94%**.
- **Maiduguri** recorded the lowest humidity at **44%**.
- **Overcast clouds** was the most common weather condition, occurring in two of the five cities.
- Kaduna was the only city in the dataset reporting **light rain** at the time of data collection.

## Data Quality

The processed dataset was checked for common data quality issues.

| Check | Result |
|---|---:|
| Number of cities | 5 |
| Missing values | 0 |
| Duplicate records | 0 |
| Dataset format | CSV |

## Visualizations

The project includes visualizations comparing:

- Temperature across the five cities
- Humidity across the five cities

These visualizations help make differences between the cities easier to understand.

## Project Structure

```text
Week_7_Weather_ETL/
│
├── data/
│   └── processed_weather_data.csv
│
├── .env
├── .gitignore
├── README.md
├── requirements.txt
└── weather_etl.ipynb