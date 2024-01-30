# Predictive Trading Strategy Development for VDE ETF Using Machine Learning

## Project Description

This project focuses on developing a predictive trading strategy for the VDE ETF (Vanguard Energy ETF) using machine learning techniques. The strategy aims to forecast whether there will be a positive or negative daily return for the ETF, as well as predict vital values for the next trading day such as Open, High, Low, Close, Daily Return, and Move_Per.

## **For more details, please refer to the [PDF report](./Trading_Strategy_for_VDE_Report.pdf).**

## Part 1: Model Selection and Evaluation
- Daily stock price data spanning nearly 20 years is collected from Yahoo Finance.
- The dataset includes features such as Open, High, Low, Volume, Daily Return, Move (High – Low), Move_Per (Move/Low), SMA_5 (Simple 5-Day Moving Average), and SMA_21 (Simple 21-Day Moving Average).
- Close price is chosen as the target variable for prediction.
- Machine learning models including Multiple Regression, Decision Tree, Random Forest, and K-NN are evaluated.
- Performance metrics such as MAE, MSE, RMSE, R-Squared, and MAPE are calculated to assess model performance.
- Different time frames are considered to evaluate the predictive power of the models.
- Residual analysis is conducted to validate model results.
- Multiple Regression and Random Forest demonstrate superior performance across various time frames.
- Both models are cross validated to finalize model selection for building the trading strategy.

## Part 2: Trading Strategy Implementation
- Users input a desired percentage profit (delta) for the day.
- A Random Forest Classifier model is trained to predict whether the next day's return will be positive (1) or negative (0).
- The best performing models from Part 1 (Multiple Regression and Random Forest) are used to predict vital values for the next trading day which are Open, High, Low, Close, Daily Return and Move_per.
- The probability of achieving the user-specified delta is calculated using a method detailed in the attached report. This method involves analyzing historical data and model predictions to estimate the likelihood of the ETF reaching the desired profit threshold on a given trading day. Further details on the probability calculation approach can be found in the provided report.
- The trading strategy integrates both machine learning predictions and user-defined profit goals to inform trading decisions.

This project aims to leverage machine learning to enhance trading decision-making processes and optimize returns for investors in the VDE ETF.


