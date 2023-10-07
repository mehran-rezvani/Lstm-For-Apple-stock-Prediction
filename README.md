# Lstm-For-Apple-stock-Prediction
This Python code is a straightforward example of using a Long Short-Term Memory (LSTM)
neural network to predict the stock price of Apple Inc. It uses historical stock price data for training and then makes predictions for future stock prices. Here's a concise explanation of the code in 10 lines:

Import necessary libraries: NumPy for numerical operations, Matplotlib for plotting, Pandas for data manipulation, and scikit-learn's MinMaxScaler for data scaling.
Read historical Apple stock price data from a CSV file ("AAPL.xls") into a Pandas DataFrame named "apple_training_complete."
Extract the 'Open' price column from the DataFrame and store it in the "apple_training_processed" variable as a NumPy array.
Use MinMaxScaler to scale the stock prices to the range [0, 1] and store the scaled data in "apple_training_scaled."
Create lists "features_set" and "labels" to prepare training data. Iterate through the scaled data to create sequences of 60 consecutive stock prices (features) and their corresponding next-day prices (labels).
Convert "features_set" and "labels" to NumPy arrays.
Reshape the "features_set" array to match the expected input shape for the LSTM model.
Import the necessary libraries from Keras for building a sequential LSTM model with dropout layers.
Define the architecture of the LSTM model with multiple LSTM layers and a dense output layer. Compile the model with the 'adam' optimizer and mean squared error loss.
Read testing data from another CSV file ("AAPL - Jan2018.xls"), preprocess it similarly to the training data, make predictions using the trained model, and plot the actual and predicted stock prices.
The code essentially performs data preprocessing, builds an LSTM model for time-series prediction, trains it on historical data, and evaluates its performance by predicting future stock prices and visualizing the results.
