# TimeSeries_Forecast_of_UAN32_NOLA
This study analyzes UAN32_NOLA prices using SARIMAX time series modeling. It covers preprocessing, stationarity testing, model building, and evaluation. Findings show SARIMAX achieves moderate forecasting accuracy, but further optimization and comparison with baseline models are needed for improved reliability.

## Overview
This repository contains a comprehensive time series forecasting project focused on predicting UAN32_NOLA prices using the SARIMAX model with exogenous variables from agricultural and energy markets.

## Project Structure
text
UAN32_Forecast_SARIMAX/
│
├── data/
│   └── UAN32_data.csv
│
├── notebooks/
│   └── UAN32_SARIMAX_Forecast.ipynb
│
├── src/
│   ├── preprocessing.py
│   ├── model.py
│   └── visualization.py
│
├── requirements.txt
├── README.md
└── TimeSeries_Forecast_of_UAN32_NOLA.pdf
Installation
bash
git clone https://github.com/your_username/UAN32_Forecast_SARIMAX.git
cd UAN32_Forecast_SARIMAX
pip install -r requirements.txt
Usage
bash
jupyter notebook notebooks/UAN32_SARIMAX_Forecast.ipynb
Dataset
The analysis utilizes a dataset with the following variables:

Target Variable: UAN32_NOLA prices

Exogenous Variables:

Ammonia (4-week EMA)

UAN Baltic Sea prices

Ethanol prices

Coal prices

Dutch Natural Gas (4-week MA)

Urea Midwest prices

Methodology
Data Preprocessing: DateTime indexing and missing value handling

Stationarity Testing: Augmented Dickey-Fuller test

Seasonal Decomposition: Additive model decomposition

SARIMAX Modeling: Parameter optimization using AIC values

Performance Evaluation: RMSE and MAE metrics

Results
Best Model: SARIMAX with optimized parameters

RMSE: 10.33

MAE: 7.15

Significant Variables: Ammonia (4-week EMA), UAN Baltic Sea prices, Urea Midwest prices

Forecast Results
Date	Forecasted Price
2025-01-16	255.14
2025-01-23	253.33
2025-01-30	253.21
2025-02-06	251.94
2025-02-13	251.68
2025-02-20	252.25
2025-02-27	252.21
2025-03-06	251.02
2025-03-13	250.82
2025-03-20	251.46
2025-03-27	251.48
2025-04-03	250.35
Dependencies
Python 3.7+

pandas

numpy

statsmodels

matplotlib

seaborn

jupyter

License
This project is licensed under the MIT License.

Contact
For questions about this project, please open an issue in the GitHub repository.

Note: This is a research project for analytical purposes. Forecasts should be validated with current market data before making business decisions.

Copy and paste this content into a file named README.md in your project directory.
