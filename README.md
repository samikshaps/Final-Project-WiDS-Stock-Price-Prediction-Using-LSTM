# Stock Price Prediction Using LSTM

## Overview

This project is focused on predicting future stock prices using **Long Short-Term Memory (LSTM)**, a type of recurrent neural network (RNN) known for its ability to model sequential data. The implementation includes data collection, visualization, feature engineering, model training, and forecasting future stock prices.

---

## Project Description

The project involves the following key steps:

1. **Data Collection**  
   Using the `yfinance` library, stock price data (historical) is downloaded for a user-specified stock ticker, time frame, and date range. 

2. **Data Visualization**  
   Visualizations are created to analyze trends and identify patterns using technical indicators like:
   - **Adjusted Closing Price** over time.
   - **Moving Average Convergence Divergence (MACD)** to identify trend reversals.
   - **Simple Moving Average (SMA)** and **Exponential Moving Average (EMA)** to track trends smoothly.

3. **Data Preprocessing**  
   - Data is scaled using **Min-Max Scaling** to normalize it between 0 and 1, ensuring better performance of the LSTM model.
   - Overlapping sliding windows are created as input sequences for the LSTM model.

4. **LSTM Model Development**  
   A two-layer LSTM model is designed to capture the temporal patterns in the stock prices. The model predicts the next closing price based on past trends.

5. **Evaluation and Prediction**  
   - The model's performance is evaluated using the **Mean Squared Error (MSE)** and **R² score**.
   - Predictions for the next 15 time steps are made and visualized.

---

## Technical Indicators Used

1. **Adjusted Close Price**  
   Reflects the stock's actual value after accounting for events like dividends and splits. Useful for comparing prices over time.

2. **Moving Average Convergence Divergence (MACD)**  
   - Formula: `MACD = Short EMA (12) - Long EMA (26)`  
   Indicates the strength and direction of a trend. Positive values suggest an uptrend, and negative values suggest a downtrend.

3. **Simple Moving Average (SMA)**  
   - Formula: `SMA = Average(Close Prices over n days)`  
   Useful for smoothing short-term fluctuations and highlighting trends.

4. **Exponential Moving Average (EMA)**  
   - Similar to SMA but gives more weight to recent data. Useful for quicker trend identification.

---

## Results

1. **Visualization Insights**  
   - Stock price trends over time were effectively captured.
   - SMA and EMA highlighted both short-term and long-term trends.

2. **Model Performance**  
   - Loss (MSE) was minimized during training and testing phases.
   - The R² score provides an indication of how well the model fits the data.

3. **Future Predictions**  
   The model successfully predicted stock prices for the next 15 time steps, offering insights into possible future trends.

---

## Instructions to Run the Code

## Prerequisites
   Ensure the following libraries are installed:
   - `pandas`
   - `numpy`
   - `yfinance`
   - `matplotlib`
   - `seaborn`
   - `sklearn`
   - `tensorflow`

   Install them using:
   pip install pandas numpy yfinance matplotlib seaborn scikit-learn tensorflow

## Running the Script

1. **Clone or Download the Script**  
   Clone the repository or download the script to your local machine.

2. **Execute the Script**  
   Run the script in your Python environment.

3. **Enter the Following Inputs When Prompted**:  
   - **Stock ticker symbol** (e.g., `AAPL` for Apple, `GOOGL` for Alphabet Inc.)  
   - **Start date** (e.g., `2020-01-01`)  
   - **End date** (e.g., `2023-01-01`)  
   - **Time frame** (e.g., `1d`, `1wk`, `1mo`)  

---

## Interpreting the Output

1. **Visualize Stock Trends and Technical Indicators**  
   Review the plots to understand stock price trends, SMA, EMA, and MACD patterns.

2. **Examine Model Performance**  
   - Look at training and testing loss values.
   - Evaluate the **R² score** for model accuracy.

3. **Analyze Future Predictions**  
   Use the forecasted prices for the next 15 time steps to derive actionable insights.

---

## Key Takeaways

### Significance of LSTM
- LSTM is highly effective for sequential data analysis.  
- It is ideal for time-series forecasting tasks, such as stock price prediction.

### Role of Technical Indicators
- Indicators like **MACD**, **SMA**, and **EMA** provide valuable insights into market trends.
- They help to inform and improve the model's predictive capabilities.

---

## Future Scope

1. **Enhanced Feature Engineering**  
   - Include additional indicators like **RSI (Relative Strength Index)** or **Bollinger Bands** to refine predictions.

2. **Sentiment Analysis**  
   - Integrate sentiment analysis using news or social media data to improve accuracy and provide a more comprehensive prediction model.




