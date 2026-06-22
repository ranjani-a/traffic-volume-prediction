# Metro Interstate Traffic Volume -- Ensemble Model Comparison

Week 3 statistics task. Comparing Random Forest, AdaBoost, and XGBoost on the UCI Metro Interstate Traffic Volume dataset.

**Dataset:** https://archive.ics.uci.edu/dataset/492/metro+interstate+traffic+volume  
**Task:** Regression -- predict hourly traffic volume on I-94 between Minneapolis and St Paul, MN  
**Data:** 48,204 hourly records from October 2012 to September 2018

## What is in the notebook

1. Load and inspect the raw data
2. Data cleaning (0 Kelvin temps, impossible rain values, duplicate rows, holiday label fix)
3. Feature engineering (time features, cyclic encodings, rush hour flag)
4. Exploratory data analysis (hourly patterns, day-of-week effects, weather impact, correlations)
5. Time-aware train/test split (train on 2012-2017, test on 2018)
6. Random Forest -- hyperparameter tuning + feature importance
7. AdaBoost -- learning rate and n_estimators grid search + staged error plot
8. XGBoost -- grid search + early stopping + learning curve
9. Full model comparison (MAE, RMSE, R2, MAPE, residual plots, time series view)
10. Cross-validation comparison
11. Feature importance comparison across all three models
12. Summary and conclusions

## Setup

```bash
pip install -r requirements.txt
```

Download the dataset from the UCI link above and save it as `Metro_Interstate_Traffic_Volume.csv` in the same folder as the notebook.

Then open the notebook:

```bash
jupyter notebook traffic_analysis.ipynb
```

Or in VS Code: open the `.ipynb` file directly and select your Python kernel.

## Results summary

| Model | MAE | RMSE | R2 |
|---|---|---|---|
| Random Forest | see notebook | see notebook | see notebook |
| AdaBoost | see notebook | see notebook | see notebook |
| XGBoost | see notebook | see notebook | see notebook |

XGBoost achieves the best scores overall. Random Forest is very close. AdaBoost trails due to sensitivity to noise and outliers in the dataset.

The most important predictor is hour of day, followed by day of week and the engineered rush-hour flag. Weather features add a small but real signal on top of the time features.
