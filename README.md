# Stock Price Prediction using LSTM

This project involves predicting the stock price of a company using Long Short-Term Memory (LSTM) networks. It utilizes historical stock data to forecast future stock prices and visualizes the results.

## Libraries Used

- `pandas`: For data manipulation and analysis.
- `numpy`: For numerical operations and array handling.
- `yfinance`: For retrieving historical stock data.
- `matplotlib`: For data visualization.
- `seaborn`: For enhanced plotting.
- `sklearn`: For preprocessing and evaluation metrics.
- `tensorflow`: For building the LSTM model.

## Project Steps

### 1. Data Collection
- **User Input**: The program prompts the user to enter the stock ticker symbol, start and end date, and time frame (e.g., 1d, 1wk).
- **Data Retrieval**: Using `yfinance`, the program downloads historical stock data for the specified ticker symbol, start date, and end date.

### 2. Data Visualization
- **Stock Closing Price**: The program visualizes the stock's adjusted closing price over time using `matplotlib`.
- **MACD Plot**: It calculates and plots the Moving Average Convergence Divergence (MACD), which is used to analyze stock price trends.
- **SMA/EMA**: The program also visualizes Simple Moving Average (SMA) and Exponential Moving Average (EMA) for stock price analysis.

### 3. Data Preprocessing
- **Min-Max Scaling**: The data is normalized using the `MinMaxScaler` to scale the features between 0 and 1.
- **Sliding Window Creation**: The program prepares the data in overlapping sequences for use in training an LSTM model. A window size of 40 is used to create sequences of historical stock data.

### 4. Build the LSTM Model
- **Data Splitting**: The dataset is split into training and testing sets.
- **LSTM Model**: The LSTM model consists of two layers with 50 neurons each. The model is trained for 20 epochs using the Adam optimizer and Mean Squared Error loss function.

### 5. Prediction and Visualization
- **Forecasting**: The model predicts stock prices for the next 15 units of time after training on the historical data.
- **Visualization**: The predictions are visualized alongside the actual training and testing data to evaluate the model's performance.
- **R² Score**: The program calculates the R² score to measure the accuracy of the model's predictions.

## Example Workflow

### Input:
- **Stock Symbol**: `AAPL` (Apple)
- **Start Date**: `2020-01-01`
- **End Date**: `2023-01-01`
- **Time Frame**: `1d`

### Output:
- **Stock Closing Price Plot**: A plot showing the adjusted closing price over the given time period.
- **MACD Plot**: A plot showing the MACD values.
- **SMA and EMA Plots**: A comparison of Simple and Exponential Moving Averages.
- **Predicted Prices**: A plot showing the forecasted stock prices for the next 15 days.
- **R² Score**: A numerical measure of the model's prediction accuracy.

