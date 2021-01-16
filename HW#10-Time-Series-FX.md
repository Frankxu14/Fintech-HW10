# Unit 10—A Yen for the Future
Frank Xu


## Background

The financial departments of large companies often deal with foreign currency transactions while doing international business. As a result, they are always looking for anything that can help them better understand the future direction and risk of various currencies. Hedge funds, too, are keenly interested in anything that will give them a consistent edge in predicting currency 


In this Homework assignment, we apply  Time Series Forecasting and Linear Regression Modeling to predict future movements in the value of the Japanese yen versus the U.S. dollar.

## Time Series Forecasting
The code first load historical Dollar-Yen exchange rate futures data and apply time series analysis and modeling to determine whether there is any predictable behavior.
The steps outlined in the time-series notebook include the following:

1. Decomposition using a Hodrick-Prescott Filter (Decompose the Settle price into trend and noise).
2. Forecasting Returns using an ARMA Model.
3. Forecasting the Settle Price using an ARIMA Model.
4. Forecasting Volatility with GARCH.

Based upon the results of the time series analysis and modeling, I answer the questions as follows:
1. Based on your time series analysis, would you buy the yen now?
2. Is the risk of the yen expected to increase or decrease?
3. Based on the model evaluation, would you feel confident in using these models for trading?

Based on the above time series analysis, I probably will buy the yen futures as the price may rise per 5 Days forecast.
Pursuant to Volatility Forecasting with GARCH, risk will also rise.
Statistic summary shows the model is a reasonably good fit.

However, ARMA model for predicting future returns, and ARIMA model for predicting yen futures prices both have p-values well above 0.05, and therefore need further tuning or improvement.


## Linear Regression Modeling

On the Linear Regression Forecasting, we build a Scikit-Learn linear regression model to predict Yen futures ("settle") returns with *lagged* Yen futures returns and categorical calendar seasonal effects (e.g., day-of-week or week-of-year seasonal effects).

The key steps outlined in the regression_analysis notebook includes
Data Preparation; Fitting a Linear Regression Model; Making predictions using the testing data; Calculate Out-of-sample performance (MSE and RMSE) and In-sample performance.

The results show the model perform better on out-of-sample data compared to in-sample data. Based on the above SKLearn Linear Regression analysis: The model produces an Out-of-sample Root Mean Squared Error (RMSE) of about 0.415 and an In-sample Root Mean Squared Error (RMSE) of about 0.596.

Normally we expect higher error rate on the Out-of-sample data not vice versa; as the model is trained and to make optimal prediction based on the In-sample-data.