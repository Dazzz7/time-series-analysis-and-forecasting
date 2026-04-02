# ✈️ Time Series Forecasting of Airfares (33 Years)
📌 Project Overview

This project focuses on forecasting airline fares using historical data spanning over 33 years (1989–2022). The goal is to analyze trends, seasonality, and patterns in airfare prices and build accurate forecasting models.

I implement and compare multiple time series models, including ARIMA and SARIMA, to determine the most effective approach for predicting future airfare trends.

## Live Demo
## https://colab.research.google.com/drive/1wb-mfi660geMHVxmu-PXz5n9KvMmmJ1j?usp=sharing

📊 Dataset
Source: Federal Reserve Economic Data (FRED)
Dataset Link: https://fred.stlouisfed.org/series/CUSR0000SETG01

⚙️ Libraries used:
 NumPy, Pandas, Matplotlib, Seaborn, Statsmodels (ARIMA, SARIMAX), Prophet, Scikit-learn, SciPy

🔍 About the project:
The project begins with a thorough understanding of the dataset. The data is loaded and inspected to analyze its structure, dimensions, and data types. Summary statistics are generated to gain initial insights into the distribution of airfare values, and checks are performed to confirm that there are no missing values in the dataset.

Following this, Exploratory Data Analysis (EDA) is conducted to uncover patterns and trends in the data. Time series plots are used to visualize how airfare prices have evolved over time, while histograms and boxplots help understand the distribution and detect any anomalies. From this analysis, a clear upward trend and recurring seasonal patterns are observed, along with a noticeable drop in airfare prices around 2020, likely due to the impact of the COVID-19 pandemic.

In the data preparation phase, the dataset is cleaned and transformed for modeling. The date column is converted into a datetime format and set as the index to enable time series analysis. The airfare column is renamed for clarity. To stabilize variance and prepare the data for modeling, transformations such as Box-Cox are applied, followed by differencing to remove trends and achieve stationarity. Linear interpolation is also explored for smoothing purposes.

Next, time series decomposition is performed to break down the data into its underlying components: trend, seasonality, and residuals. Both additive and multiplicative decomposition methods are used, confirming that the dataset contains strong seasonal and trend components, which are important considerations for model selection.

To ensure the suitability of time series models, stationarity is tested using the KPSS test. The results initially indicate that the series is non-stationary. After applying transformations and differencing, the test is repeated, confirming that the series has become stationary and is ready for modeling.

Further analysis is conducted using Auto-Correlation Function (ACF) and Partial Auto-Correlation Function (PACF) plots. These help identify the relationship between current and past values, revealing strong correlations across time lags. This insight is critical for selecting appropriate parameters for time series models such as ARIMA and SARIMA.

Finally, the dataset is split into training and testing sets to evaluate model performance. Multiple forecasting models, including ARIMA and SARIMA, are built and tested. Their performance is compared using evaluation metrics such as RMSE and MAPE. Additionally, different parameter configurations and train-test splits are experimented with to improve model accuracy and robustness.

🙌 Acknowledgements
Data Source: FRED (Federal Reserve Bank of St. Louis)
Libraries: Statsmodels, Scikit-learn, Prophet
