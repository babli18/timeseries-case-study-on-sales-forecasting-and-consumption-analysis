**End-to-End Time Series Analysis: Sales and Consumption Case Studies**
========================================================================
## **Purpose**
This notebook is designed to demonstrate end-to-end time series analysis and forecasting using various statistical methods, focusing on two datasets: retail drug sales and wine consumption. It explores techniques like seasonal differencing, autocorrelation analysis, and SARIMA modeling to understand data patterns and make accurate predictions.


#### **Case Study 1: Pharma Drug Sales Forecasting**
- **Objective**: Forecast monthly retail sales of a pharmaceutical product over 17 years.
- **Key Steps**:
  1. **Exploratory Analysis**:
     - Plotted time series to identify seasonality and trends.
     - Used ACF to confirm a seasonal period of 12 months.
  2. **Trend Analysis**:
     - Applied a 12-month moving average to observe long-term trends.
  3. **Stationarity**:
     - Differenced the data (first and seasonal) to remove trends and seasonality.
     - Re-plotted ACF and PACF to confirm stationarity.
  4. **Model Development**:
     - Tested SARIMA configurations with different parameter combinations.
     - Selected the best model using AIC and BIC.
  5. **Forecasting**:
     - Predicted sales from July 2005 onwards using the selected SARIMA model.
     - Evaluated predictions using Mean Squared Error (MSE).
- **Outcome**:
  - The model captured seasonal patterns effectively and provided reasonable forecasts for future sales.

---

#### **Case Study 2: Wine Consumption Analysis**
- **Objective**: Analyze and model quarterly wine consumption data using an AR model.
- **Key Steps**:
  1. **Exploratory Analysis**:
     - Plotted the time series and identified a seasonal period of 4 quarters using ACF.
  2. **Seasonal Differencing**:
     - Tested differencing lags of 1, 2, 4, and 6 quarters to remove seasonality.
     - Determined lag 4 as the most effective for seasonal adjustment.
  3. **AR Model Development**:
     - Used "select_order" to determine the optimal lag for an AR(p) model after seasonal differencing.
     - Fitted an AR model using the identified lag.
  4. **Prediction**:
     - Predicted seasonally adjusted values starting at the optimal lag.
     - Compared predictions with actual seasonally differenced data.
  5. **Evaluation**:
     - Calculated Mean Absolute Error (MAE) to assess the model's accuracy.
- **Outcome**:
  - The seasonal period was successfully removed, and the AR model accurately captured the underlying patterns for wine consumption.
