# Predictive Data Modelling and Analysis

The data is from the M4 Forecasting competition and spanned over almost 10 years. Analysis was done for Series 3, Series 31, and Series 59. 

Time series, consisting of systematic and irregular components, is deconstructed  by calculating Centered Moving Averages and plotting seasonal plots, whilst conducting decomposition plots through R functions.

The time series proceeded to statistical analysis wherein Kwiatkowski-Phillips-Schmidt-Shin (KPSS) and augmented Dickey–Fuller test (ADF) statistical tests were conducted to associate trends with the data.
 
To train forecasting models, we require the data to be non-stationary i.e. no trend nor seasonality.


 KPSS	Test 
 
 Null hypothesis H0 -  Stationary <br>
 Alternative hypothesis H1 - Non-stationary

 
 ADF	Test   
 
 Null hypothesis H0 - Non-stationary	      
 Alternative hypothesis H1 - Stationary

The auto-correlation function [ACF] provides us with the auto-correlation values of any series with their lagged values. The ACF plot indicates how closely the series' present value is related to its prior values.

In the partial auto-correlation function [PACF]  we first eliminate previously observed variations, it is "partial" rather than "complete" in that it identifies correlations between the residuals that are still there after removing the effects that have already been described by the earlier lag(s) and the next lag value. 

Differencing can help stabilise the mean of a time series by removing changes in the level of a time series and therefore eliminating (or reducing) trend and seasonality.

After the data is trained, we use the ARIMA model for time-series forecasting. ARIMA is used over Exponential Smoothing as exponential smoothing models are based on a description of the trend and seasonality in the data, ARIMA models aim to describe the autocorrelations in the data.

As our data is seasonal, we propose Seasonal ARIMA models [SARIMA], 

For Series 3 the proposed models are SARIMA (1,2,0) (0,1,0) [12] and SARIMA (1,2,0) (3,1,2) [12]. <br>
For Series 31 the proposed models are SARIMA(0,2,0)(0,1,0)[12] and SARIMA(1,2,0)(0,1,0)[12]. <br>
For Series 59 the proposed models are SARIMA (1,2,0) (0,1,0) [12] and SARIMA(1,1,0)(0,1,0)[12]. 



