# Weather-Temperature-Prediction-using-RNN
A time‑series forecasting model built with TensorFlow/Keras to predict future temperatures using historical weather data. Includes preprocessing, RNN training, evaluation, and 7‑day forecasting with visualizations.
## 📌 Project Overview
This project demonstrates how RNNs can model sequential weather data and forecast future temperature values.
It includes:

-Data loading & cleaning

-Time‑series preprocessing (windowing)

-Feature scaling

-RNN model building & training

-Evaluation using MSE, MAE, R²

-Future temperature forecasting

-Visualizations for trends and predictions

## 📂 Dataset
The dataset is downloaded using KaggleHub:

Source: muthuj7/weather-dataset

File used: weatherHistory.csv

Contains temperature, humidity, wind speed, and other weather attributes

The Formatted Date column is converted to datetime and set as the index for time‑series analysis.

##🧼 Data Preprocessing
✔️ Handle Missing Values
Only the Precip Type column had missing values

Rows with missing values were removed

✔️ Feature Selection
Selected features:

Temperature (C)

Humidity

Wind Speed (km/h)

Target variable:

Temperature (C)

✔️ Normalization
Applied MinMaxScaler to scale all features to the range 0–1.

✔️ Sequence Creation
A sliding window of 7 days is used:

X: past 7 days of features

y: next day temperature

## 🧠 Model Architecture
A simple but effective RNN model:

SimpleRNN(64, activation='relu')

Dropout(0.2)

Dense(1) output layer

Compiled with:

Loss: Mean Squared Error (MSE)

Optimizer: Adam

Metric: Mean Absolute Error (MAE)

## 🏋️ Training
Trained for 50 epochs

Batch size: 32

Validation split: 15%

Loss curves show stable convergence without overfitting.

## 📊 Evaluation
Metrics on test data:

MSE: ~0.0004

MAE: ~0.0122

R² Score: ~0.9835

These results indicate excellent predictive performance.

## 🔮 Forecasting Future Temperatures
The model predicts:

Next 7 days of temperature

Using the last 7 days of scaled data

Predictions are inverse‑transformed back to °C

A combined plot shows:

Last 100 actual temperature values

Model predictions

Future 7‑day forecast

## 📈 Visualizations Included
Temperature trend over time

Training vs validation loss

Actual vs predicted temperatures

Forecast vs recent history

## 🛠️ Technologies Used
Python

Google Colab

TensorFlow / Keras

NumPy, Pandas

Matplotlib

Scikit‑learn

## 🚀 How to Run
Open the notebook in Google Colab

Install dependencies (if required)

Run all cells sequentially

Ensure KaggleHub is authenticated for dataset download

## 📜 License
This project is for educational and research purposes.
