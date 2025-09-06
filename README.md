# Time Series Forecasting of UAN32_NOLA Prices using SARIMAX

![Python](https://img.shields.io/badge/Python-3.7%2B-blue)
![Library](https://img.shields.io/badge/Library-statsmodels-orange)
![Status](https://img.shields.io/badge/Status-Complete-success)

This repository contains the code and analysis for a comprehensive time series forecasting project focused on predicting UAN32_NOLA prices, a key fertilizer product in the agricultural and energy sectors. The project leverages the SARIMAX model (Seasonal AutoRegressive Integrated Moving Average with eXogenous variables) to incorporate external market drivers and seasonal patterns.

📖 ##Abstract
Forecasting is critical for informed decision-making in volatile markets. This study presents a methodical approach to modeling and forecasting UAN32_NOLA prices. The process involves:

Data preprocessing and exploratory analysis.

Stationarity testing using the Augmented Dickey-Fuller (ADF) test.

Model development with SARIMAX, optimized using the Akaike Information Criterion (AIC).

Performance evaluation using RMSE and MAE metrics.

The results indicate that the SARIMAX model provides a moderate level of forecasting accuracy, establishing a strong foundation for further refinement and operational use.

🗃️ ##Dataset
The analysis utilizes a dataset comprising several exogenous variables relevant to agricultural and energy markets:

Target Variable: UAN32_NOLA prices

Exogenous Variables:

Ammonia (4-week EMA)

UAN Baltic Sea prices

Ethanol prices

Coal prices

Dutch Natural Gas (4-week MA)

Urea Midwest prices

The dataset consisted of 521 complete observations with no missing values.

🛠️ ##Methodology
1. Preprocessing & Exploration
Checked for and confirmed no missing values.

Performed seasonal decomposition using an additive model to identify trend, seasonality, and residual components.

2. Stationarity
The original series was non-stationary (ADF p-value: 0.198).

First-order differencing was applied to achieve a stationary series (ADF p-value: 0.001), a prerequisite for SARIMAX modeling.

3. Model Development
SARIMAX was selected for its ability to handle both seasonal patterns and exogenous variables.

Model parameters (p, d, q) and seasonal parameters (P, D, Q, s) were systematically optimized by evaluating combinations based on their AIC values.

ACF and PACF plots were analyzed to inform parameter selection.

📈 ##Key Results
Model Summary
Log Likelihood: -1900.732

AIC: 3823.465

BIC: 3870.193

Significant Variables
The following variables had a statistically significant (p < 0.001) impact on UAN32_NOLA prices:

Ammonia_4Week_EMA (Coeff: +0.3065)

UAN_BalticSea (Coeff: +0.0899)

Urea_Midwest (Coeff: +0.0754)

AR(1) (Coeff: +0.9254) - indicating strong price persistence.

Seasonal MA(4) (Coeff: -0.9877) - indicating a strong negative seasonal pattern.

Forecast Performance
Root Mean Squared Error (RMSE): 10.33

Mean Absolute Error (MAE): 7.15

The model's predictions deviate from actual values by approximately 7 to 10 units on average.

🔮 ##Forecasts
The model forecasts for the next 12 weeks (starting Jan 16, 2025) are:

Date	Forecasted Price
2025-01-16	255.14
2025-01-23	253.33
2025-01-30	253.21
2025-02-06	251.94
2025-02-13	251.68
2025-02-20	252.25
...	...
2025-04-03	250.35
(See the full list in the report above)

✅ ##Conclusion
The SARIMAX model demonstrates significant potential for forecasting UAN32_NOLA prices. The model successfully captures the influence of key market drivers and strong seasonal effects. While the current accuracy is moderate, it provides a robust baseline for future optimization.

📋 ##Recommendations for Future Work
Incorporate Additional Variables: Integrate other potential influencers like weather data, agricultural demand cycles, or global trade flow data.

Model Comparison: Compare SARIMAX performance against other advanced models like Prophet, LSTM networks, or Gradient Boosting Machines (GBM).

Automated Retraining: Implement a pipeline to regularly update the model with new data to maintain forecast accuracy over time.

Hyperparameter Tuning: Conduct a more extensive grid search for SARIMAX orders and seasonal orders to potentially find a more optimal configuration.

🚀 ###Getting Started
Prerequisites
Python 3.7+

Jupyter Notebook/Lab

###Installation
Clone the repo:

###bash
git clone https://github.com/your_username_/UAN32_Forecast_SARIMAX.git
Install required packages:

###bash
pip install -r requirements.txt
(Note: A requirements.txt file should be created listing packages like pandas, numpy, statsmodels, matplotlib, seaborn)

##Usage
Open and run the Jupyter Notebook UAN32_SARIMAX_Forecast.ipynb to see the full analysis, from data loading to forecasting.

📄 ##License
This project is licensed for academic and research purposes. Please cite this repository if you use the code or methodology.
