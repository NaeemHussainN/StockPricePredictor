# Stock Price Prediction using LSTM

This project demonstrates the use of an artificial recurrent neural network (Long Short-Term Memory, LSTM) to predict the closing stock price of META Inc. based on the stock's historical data over the past 60 days. The model uses Python and various libraries to preprocess the data, build and train the LSTM model, and visualize predictions.

## Table of Contents
- [Overview](#overview)
- [Features](#features)
- [Libraries Used](#libraries-used)
- [Dataset](#dataset)
- [Model Architecture](#model-architecture)
- [Evaluation Metrics](#evaluation-metrics)
- [Results](#results)
- [How to Run](#how-to-run)
- [Future Improvements](#future-improvements)


---

## Overview
The goal of this project is to predict the closing stock price of META Inc. using historical data from 2016 to the present. By leveraging LSTM neural networks, which are particularly adept at time-series data, the model learns patterns in stock price movements to make future predictions.

---

## Features
- Fetches stock data using Yahoo Finance.
- Preprocesses data with MinMaxScaler for LSTM input.
- Constructs and trains an LSTM model.
- Evaluates the model using Root Mean Squared Error (RMSE).
- Visualizes training data, actual prices, and predicted prices.
- Predicts future stock prices based on recent trends.

---

## Libraries Used
- **Python**: Core programming language
- **NumPy**: Numerical computing
- **Pandas**: Data manipulation
- **Matplotlib**: Data visualization
- **scikit-learn**: Data preprocessing (MinMaxScaler)
- **Keras**: Neural network implementation (LSTM)
- **yfinance**: Fetching stock data from Yahoo Finance

---

## Dataset
The dataset is fetched dynamically using the `yfinance` library to ensure it is always up-to-date with the latest stock price information and consists of the following columns:
- Open
- High
- Low
- Close
- Adjusted Close
- Volume


The model uses the "Close" column for training and predictions.

---

## Model Architecture
The LSTM model has the following structure:
1. **Input Layer**: Accepts a sequence of 60 previous closing prices.
2. **LSTM Layer**: Contains 50 units with a fully connected Dense layer.
3. **Dense Layers**: A layer with 25 units followed by the final output layer with 1 unit for prediction.
4. **Optimizer**: Adam optimizer is used for backpropagation.
5. **Loss Function**: Mean Squared Error (MSE).

---

## Evaluation Metrics
The performance of the model is evaluated using **Root Mean Squared Error (RMSE)**:
- Lower RMSE indicates better predictions.

Result: `RMSE = 19.14`

---

## Results
The model successfully predicts future stock prices for META Inc. with a reasonable degree of accuracy:
- Predicted price for the next day: `$596.66`
- Actual price for the next day: `$585.25`
- Result from: December 21st, 2024

![Model Predictions](https://github.com/NaeemHussainN/StockPredictorML/blob/main/StockModel.png)

---

## How to Run
### Prerequisites
Ensure you have Python installed along with the following libraries:
```bash
pip install numpy pandas matplotlib scikit-learn keras yfinance
```

### Steps
1. Clone the repository:
   ```bash
   git clone https://github.com/NaeemHussainN/StockPredictorML.git

   cd StockPricePredictor
   ```
2. Run the Python script:
   ```bash
   python stock_price_predictor.py
   ```
3. View the visualizations and predictions generated by the model.

---

## Future Improvements
- Use more advanced models like Transformer-based architectures for time-series prediction.
- Incorporate additional features like technical indicators (e.g., RSI, MACD).
- Experiment with hyperparameter tuning and model optimization.
- Extend the model to predict stock prices for multiple companies.

---

## Acknowledgements
- [Yahoo Finance](https://finance.yahoo.com/) for providing stock market data.
- [Keras](https://keras.io/) for making deep learning accessible and easy to use.

