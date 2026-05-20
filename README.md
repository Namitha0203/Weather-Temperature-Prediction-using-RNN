# 🌤️ Weather Temperature Prediction using RNN

A time-series forecasting project built in **Google Colab** using **Recurrent Neural Networks (RNN)** to predict future temperature values based on historical weather data.

---

## 📌 Project Overview
This project demonstrates how RNNs can model sequential weather data and forecast future temperature values.  
It includes:

- Data loading & cleaning  
- Time-series preprocessing (windowing)  
- Feature scaling  
- RNN model building & training  
- Evaluation using MSE, MAE, R²  
- Future temperature forecasting  
- Visualizations for trends and predictions  

---

## 📂 Dataset
- Source: Kaggle (via KaggleHub)  
- File: `weatherHistory.csv`  
- Contains temperature, humidity, wind speed, and other weather attributes  
- `Formatted Date` converted to datetime and set as index  

---

## 🧼 Data Preprocessing
- Removed missing values (only in *Precip Type*)  
- Selected features: Temperature, Humidity, Wind Speed  
- Target: Temperature  
- Applied MinMaxScaler  
- Created 7‑day sliding windows for RNN input  

---

## 🧠 Model Architecture
- `SimpleRNN(64, activation='relu')`  
- `Dropout(0.2)`  
- `Dense(1)` output layer  
- Loss: **MSE**  
- Optimizer: **Adam**  

---

## 🏋️ Training
- 50 epochs  
- Batch size: 32  
- Validation split: 15%  
- Stable convergence without overfitting  

---

## 📊 Evaluation
| Metric | Score |
|--------|--------|
| **MSE** | ~0.0004 |
| **MAE** | ~0.0122 |
| **R² Score** | ~0.9835 |

Excellent predictive performance.

---

## 🔮 Forecasting
- Predicts next **7 days** of temperature  
- Uses last 7 days of scaled data  
- Predictions inverse-transformed back to °C  

---

## 📈 Visualizations
- Temperature trend  
- Training vs validation loss  
- Actual vs predicted  
- Forecast vs recent history  

---

## 🛠️ Technologies Used
`Python` `Google Colab` `TensorFlow` `Keras`  
`NumPy` `Pandas` `Matplotlib` `Scikit-learn`

---

## 🚀 How to Run
1. Open the notebook in Google Colab  
2. Install dependencies  
3. Run all cells sequentially  
4. Ensure KaggleHub authentication  

---

## 📜 License
For educational and research purposes.

