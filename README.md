# Stock Price Prediction using LSTM

This code demonstrates how to predict stock prices using a Long Short-Term Memory (LSTM) neural network. It utilizes the historical stock price data of Tesla (TSLA) obtained from a CSV file. 

## Dependencies
- pandas
- numpy
- matplotlib
- scikit-learn
- keras

## Usage
1. Make sure you have the required dependencies installed.
2. Place the `Tesla.csv` file in the same directory as this script.
3. Run the script.

## Explanation
1. The code starts by importing the necessary libraries: `pandas`, `numpy`, `matplotlib.pyplot`, and `keras`.
2. It reads the stock price data from the CSV file into a pandas DataFrame.
3. The shape of the DataFrame is printed to get an idea of the number of rows and columns in the data.
4. The DataFrame is then modified to remove the unnecessary columns "Date" and "Adj Close" using the `drop` function.
5. The modified DataFrame is printed to verify the changes.
6. A line plot of the "Close" column is created using matplotlib.
7. The DataFrame is printed again to display the data.
8. The data is split into training and testing sets, with 70% of the data used for training and the remaining 30% for testing.
9. The training and testing sets are scaled using the MinMaxScaler from scikit-learn.
10. The training data is transformed into input sequences and target values, where each input sequence contains 100 consecutive closing prices.
11. A LSTM model is created using the Sequential class from keras. It consists of three LSTM layers and a dense output layer.
12. The model summary is printed to show the architecture and the number of parameters.
13. The model is compiled with the Adam optimizer and mean squared error loss.
14. The model is trained on the training data for 20 epochs.
15. The last 100 days of the training data are combined with the testing data to create the final DataFrame for prediction.
16. The final DataFrame is scaled using the MinMaxScaler.
17. The scaled data is printed.
18. The LSTM model is used to predict the stock prices.
19. The predicted prices are inverse transformed to obtain the actual stock prices.
20. The predicted prices are printed.

Note: The code assumes that the input CSV file has a specific format and column names. Modify the code accordingly if your data has a different structure.
