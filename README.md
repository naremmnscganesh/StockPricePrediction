
### Project Title: Stock Price Prediction using LSTM

#### Description
This project demonstrates how to predict future stock prices using a Long Short-Term Memory (LSTM) neural network. LSTMs are a type of recurrent neural network (RNN) well-suited for time-series data like stock prices. The model is trained on historical stock price data for Tata Global Beverages Limited (found in the `NSE-Tata_Global_Beverages_Limited.csv` file) to learn patterns and make predictions.

#### Key Features
* **Data Preprocessing**: The project uses the `pandas` library to load and preprocess the stock data. This includes converting the 'Date' column to a datetime object and setting it as the index, as well as using `MinMaxScaler` from `sklearn` to normalize the 'Close' price data for better model performance.
* **Time-Series Data Preparation**: A function `create_dataset` is implemented to transform the time-series data into a supervised learning format, where past data (a `time_step` of 60 days) is used to predict the next day's closing price.
* **LSTM Model Architecture**: A sequential Keras model is built with three LSTM layers, each followed by a Dropout layer to prevent overfitting. A Dense layer is used as the output layer to produce the final prediction.
* **Model Training**: The model is compiled with the `adam` optimizer and `mean_squared_error` loss function. It is trained for 25 epochs with a batch size of 32.
* **Evaluation**: The model's performance is evaluated using Root Mean Squared Error (RMSE) on a test set. The predictions are then visualized against the actual stock prices to show how well the model performs.
* **Visualization**: The project includes a plot that visualizes the historical training data, the actual stock prices in the test set, and the model's predictions, providing a clear comparison of the model's accuracy.

#### Technologies Used
* Python
* Jupyter Notebook
* `pandas`
* `numpy`
* `matplotlib`
* `scikit-learn`
* `tensorflow`
* `keras`
