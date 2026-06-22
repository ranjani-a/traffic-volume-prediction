Traffic Volume Prediction

Comparing three ensemble models on the UCI Metro Interstate Traffic Volume dataset. The data covers hourly traffic on I-94 between Minneapolis and St Paul, MN from 2012 to 2018, with weather conditions and holiday info included.

The task

Predict hourly traffic volume using weather data, time of day, and day of week. This is a regression problem.

Models compared


Random Forest
AdaBoost
XGBoost


What the notebook covers


Data cleaning (impossible temperature and rainfall values, duplicate rows, broken holiday labels)
Feature engineering (rush hour flag, cyclic time encodings, weekend flag)
EDA with plots for hourly patterns, day-of-week effects, weather impact, and correlations
Hyperparameter tuning for all three models
Full comparison across MAE, RMSE, R2, and MAPE
Residual plots, actual vs predicted, and a time series view of predictions
Feature importance comparison across all three models