# Walmart Sales Prediction Project

## Overview
This project predicts weekly sales for Walmart stores using historical sales data, store information, and economic features. The model incorporates **time series features**, **lag features**, **rolling averages**, and **seasonal decomposition** to improve prediction accuracy. Multiple models like **XGBoost**, **CatBoost**, and **LightGBM** are explored.

---

## Datasets
The project uses three CSV files:

1. **train.csv** - Historical weekly sales for each store and department.
2. **stores.csv** - Store metadata including type and size.
3. **features.csv** - Weekly economic indicators and holiday flags.

All datasets are merged into a single DataFrame for preprocessing and modeling.

---

## Feature Engineering
1. **Date Features:** Extract `Year`, `Month`, `Week`, `Day`, `DayOfWeek`.
2. **Lag Features:** Previous 1-4 week sales for each store-department combination.
3. **Rolling Averages:** 1-4 week rolling mean of weekly sales.
4. **Seasonal Decomposition:** Capture seasonal trends for each store-department.
5. **Store/Dept Aggregates:** Average sales per store and per department.
6. **Categorical Features:** Store, Dept, Type, IsHoliday.

Missing values in numeric columns are filled with `0`. Categorical columns are properly encoded.

---

## Modeling

### XGBoost
- Converts `Type` to categorical
- Uses 300 estimators, learning rate 0.05, max depth 6

### CatBoost
- Iterations: 2000, learning_rate: 0.05, depth: 8
- Handles categorical features natively

### LightGBM
- Iterations: 2000, learning_rate: 0.03, num_leaves: 64, max_depth: 10
- Early stopping with 100 rounds
- Includes rolling averages, lag features, and seasonal decomposition

---
