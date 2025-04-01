# DSTI Exam - Time Series

### Summary of the Examination Exercise

#### Objective:

- **Task**: Using historical Time Series data, forecast electricity consumption for February 21, 2010, with two approaches:
  1. Without using outdoor temperature.
  2. Using outdoor temperature as a covariate.

- **Data**: Electricity consumption and outdoor temperature recorded every 15 minutes from January 1, 2010, to February 20, 2010. Outdoor temperature data is available up to February 21, 2010.

- **Deliverables**:
  - An Excel file with two columns of 96 rows each, containing the forecasts.
  - A short report explaining the methodology, including R codes used.

### Main Results from the Report

#### Methodology:

- **Data Preparation**:
  - Data was split into training (January 1 to February 19) and testing (February 20) sets.
  - Missing or unusual data points were interpolated.

- **Models Tested**:
  - SARIMA, NNetAR, Random Forest, XGBoost, and Partial Least Squares (PLS) regression.
  - Models were evaluated with and without outdoor temperature as a covariate.
  - Both daily (96 values/day) and weekly (672 values/week) seasonality were considered.

#### Key Findings:

- **Best Model Without Covariate**:
  - ARIMA(5,0,0)(0,1,0)[96] achieved the lowest testing RMSE of 5.9.
  - Random Forest also performed well but showed overfitting issues with XGBoost.

- **Best Model With Covariate**:
  - ARIMA(5,0,0)(0,1,0)[96] with outdoor temperature achieved the same RMSE of 5.9.
  - Including outdoor temperature did not significantly improve forecast accuracy.

- **Weekly Seasonality Models**:
  - Generally performed worse than daily models, indicating overfitting.

- **Residual Analysis**:
  - Residuals did not consistently exhibit white noise properties, suggesting room for model improvement.

#### Conclusion:
- ARIMA(5,0,0)(0,1,0)[96] was the best-performing model overall.
- Forecasts aligned well with observed patterns, but residual analysis indicated potential for further refinement.
- Outdoor temperature had limited impact on improving forecast accuracy.
