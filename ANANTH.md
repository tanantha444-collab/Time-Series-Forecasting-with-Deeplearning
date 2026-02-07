Title

Multivariate Time Series Forecasting Using LSTM with Attention Mechanism

Abstract

This project addresses the problem of multivariate time series forecasting using a real-world household power consumption dataset obtained from the UCI Machine Learning Repository. A traditional statistical baseline model (ARIMA) and a deep learning model (LSTM with attention mechanism) were implemented and compared. Data preprocessing, normalization, and sequence modeling were performed systematically. Experimental results demonstrate that the proposed LSTM with attention mechanism outperforms the baseline ARIMA model in terms of RMSE and MAE, highlighting its effectiveness in capturing long-term temporal dependencies.

1. Introduction

Time series forecasting is essential in energy management, demand prediction, and smart grid applications. Traditional statistical approaches such as ARIMA rely on linear assumptions and struggle with complex temporal dependencies. Deep learning models, particularly Long Short-Term Memory (LSTM) networks, are well-suited for sequential data. This project enhances LSTM performance by integrating an attention mechanism to focus on relevant time steps.

2. Problem Statement

The objective of this project is to accurately forecast household power consumption using multivariate time-series data while comparing traditional and deep learning-based approaches. The challenge lies in handling multiple correlated variables, non-linearity, and temporal dependencies.

3. Dataset Description

A publicly available dataset was used in this project:

Dataset Name: Household Power Consumption
Source: UCI Machine Learning Repository

Features:

Global_active_power (Target variable)

Global_reactive_power

Voltage

Global_intensity

Sub_metering_1

Sub_metering_2

Sub_metering_3

The dataset contains minute-level power consumption records with missing values and temporal patterns.

4. Data Preprocessing

Missing values were handled using forward fill

Datetime features were converted into time-indexed format

All numerical features were normalized using MinMaxScaler

Sliding window approach with sequence lengths of 24 and 48 was applied

Data split:

80% Training

20% Testing

5. Baseline Model

A traditional ARIMA model was implemented as the baseline forecasting approach.

Baseline Evaluation:

RMSE: Higher

MAE: Higher

The baseline model served as a reference point for evaluating the deep learning model.

6. Proposed Methodology
6.1 LSTM with Attention Architecture

LSTM layer to capture sequential dependencies

Attention mechanism to emphasize relevant time steps

Fully connected output layer for prediction

The attention mechanism enables the model to selectively focus on important temporal information, improving prediction accuracy.

6.2 Hyperparameter Tuning

The following hyperparameters were experimentally evaluated:

Sequence length: 24, 48

LSTM units: 64, 128

Epochs: 40–60

The optimal configuration was selected based on validation performance.

7. Evaluation Metrics

The following standard forecasting metrics were used:

Root Mean Squared Error (RMSE)

Mean Absolute Error (MAE)

Mean Absolute Percentage Error (MAPE) (supporting metric)

These metrics provide a reliable assessment of forecasting performance.

8. Results and Discussion

The LSTM with attention model consistently outperformed the ARIMA baseline.

Performance Comparison:

ARIMA: Higher RMSE and MAE

LSTM + Attention: Lower RMSE and MAE

The results confirm that the attention-based deep learning model captures complex temporal dependencies more effectively than traditional approaches.

9. Conclusion

This project demonstrated the successful application of an LSTM with attention mechanism for multivariate time series forecasting using a real-world dataset. Compared to the ARIMA baseline, the proposed model achieved superior predictive performance. The findings highlight the importance of attention mechanisms in enhancing deep learning-based forecasting systems.

10. Future Scope

Transformer-based forecasting models

Multi-step ahead forecasting

Integration with real-time smart grid systems

References

Hochreiter, S., & Schmidhuber, J. (1997). Long Short-Term Memory

Vaswani et al. (2017). Attention Is All You Need

UCI Machine Learning Repository – Household Power Consumption Datas
