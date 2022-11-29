# Forecasting-Green-Energy
SARIMAX model to forecast hourly energy consumption for 3 years

1. Time series has 1900 missing values. Interpolation done.
2. Checking stationarity using ADF and KPSS tests
3. p-value for ADF test is <0.05. We reject the null hypothesis that the series is non-stationary.
4. p-value for KPSS test is <0.05. We reject the null hypothesis that the series is stationary.
5. Both tests give contradictory results. Performing both tests on lag-1 of the series.
6. The lag-1 of the series is stationary according to both the tests.
7. Plotting ACF and PACF plots of lag-1 of the series to determine the values of p and q for the ARIMA model.
8. We cannot determine p and q from ACF and PACF plots for seasonal ARIMA model. Running an auto ARIMA model to determine
9. Series has a seasonality of 24. d=1, m=24. From auto arima, we get p=0, q=2, P=1, Q=0
10. Fitting a SARIMAX model with above parameters and forecasting 3 years of data.
