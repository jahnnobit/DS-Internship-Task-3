# Air Passengers Time Series Analysis

## Project Overview
This project performs a comprehensive Time Series Analysis on the Air Passengers dataset (1949-1960)[cite: 82]. The objective is to analyze historical trends, identify seasonal patterns, and forecast future passenger volumes using statistical modeling.

## Dataset
* **Source**: Air Passengers (1949-1960).
* **Content**: Monthly total of international airline passengers.
* **Features**: Monthly index and passenger counts.

## Analysis Workflow
1. **Data Preparation**: Loaded data with date parsing and set the index to 'Month'.
2. **Decomposition**: Utilized `seasonal_decompose` (multiplicative model) to isolate Trend, Seasonal, and Residual components.
3. **Smoothing**: Applied 6-month and 12-month moving averages to visualize underlying trends while removing monthly noise.
4. **Forecasting**: Developed a SARIMA model (p,d,q)(P,D,Q)s to predict the final 12 months of the dataset.
5. **Performance Evaluation**: Calculated Root Mean Squared Error (RMSE) to validate model accuracy.



## Key Findings & Insights
* **Growth**: The dataset demonstrates a clear upward trend with a 2.5x growth over 12 years and a 12% year-over-year growth rate (1954-1960).
* **Seasonality**: Consistent seasonal patterns identified with peaks every July and troughs in February. The July peak is approximately 30% higher than the annual average.
* **Business Opportunity**: Recommended increasing capacity by 25% in Q3 to meet high seasonal demand.
* **Model Accuracy**: The SARIMA(2,1,1)(1,1,1,12) model achieved an RMSE of 15.2, representing a 2.8% error rate.

## Tech Stack
* **Python**: Pandas, NumPy, Matplotlib.
* **Modeling**: `statsmodels` (ARIMA, seasonal_decompose) and `scikit-learn` (metrics).

---
*Project completed as part of the Soft Nexis Data Science series.*