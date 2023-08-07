# Stock_Prediction

# Project Title: Stock Price Prediction using LSTM
## Description:
This project demonstrates stock price prediction using LSTM (Long Short-Term Memory) neural networks. We utilize historical stock price data for Apple Inc. (AAPL) obtained from Yahoo Finance and build an LSTM model to predict future stock prices. The model is trained on a portion of the data and tested on unseen data to evaluate its predictive performance.
## Procedure:
1. Data Collection: Historical stock price data for AAPL is fetched from Yahoo Finance using the yfinance library. The data includes daily closing prices from '2012-01-01' to '2023-07-18'.
2. Data Preprocessing: The closing price data is scaled using Min-Max normalization to bring it into the range of [0, 1], which is beneficial for training neural networks. We also split the data into training and testing sets. The training set contains 80% of the data, and the testing set contains the remaining 20%.
3. Model Architecture: We build an LSTM neural network using Keras. The model consists of two LSTM layers with 50 units each, followed by two dense layers with 25 and 1 unit, respectively. The model is compiled using the Adam optimizer and the mean squared error (MSE) loss function.
4. Model Training: The model is trained on the training dataset with a batch size of 1 and 10 epochs. The LSTM layers enable the model to capture temporal dependencies in the stock price data.
5. Prediction: The trained model is used to predict future stock prices. We select the last 60 days of closing prices from the testing dataset as input to the model for prediction. The predicted values are then scaled back to their original range using inverse transformation.
Visualization: We visualize the actual and predicted stock prices on a plot for better understanding and evaluation.
## Technologies Used:
- Python: The programming language used for the implementation of the project.
- Keras: A high-level neural networks API, running on top of TensorFlow, used to build and train the LSTM model.
- TensorFlow: The deep learning framework, on which Keras is built, used for mathematical operations and model execution.
- yfinance: A library used for fetching historical stock price data from Yahoo Finance.
  pandas, numpy, matplotlib: Libraries used for data manipulation, numerical computations, and visualization.
