# LSTM Stock Price Predictor

This project uses a Recurrent Neural Network architecture, specifically **LSTM (Long Short-Term Memory)**, to predict the **closing stock price** of a company (Google: `GOOG`) based on historical data.

---

## 🔍 Overview

Stock market prices exhibit time-dependent patterns. LSTM networks are ideal for time-series data because they can learn long-term dependencies. This project leverages an LSTM model trained on historical stock prices to predict future trends in closing prices.

---

## 📂 Project Workflow

1. **Data Collection:**
   - Used `yfinance` API to collect Google stock data from 2012 to 2023.

2. **Data Preprocessing & EDA:**
   - Checked for null values (none found).
   - Visualized closing price trends.
   - Normalized the data using `MinMaxScaler`.
   - Created a 60-day sliding window to form training sequences.

3. **Model Building:**
   - Built a Sequential LSTM model with 2 LSTM layers and 2 Dense layers.
   - Compiled with `adam` optimizer and `mean_squared_error` loss function.

4. **Training & Evaluation:**
   - Trained on 80% of the dataset.
   - Evaluated on 20% using **Root Mean Square Error (RMSE)**.
   - Plotted real vs predicted closing prices.

5. **Prediction:**
   - Model used to predict closing price based on the last 60 days.

---

## ⚙️ Technologies Used

- Python
- Pandas, NumPy
- Matplotlib
- Scikit-learn (MinMaxScaler)
- Keras (TensorFlow backend)
- yfinance

---

## 🌐 Project Structure

```
LSTM-Stock-Predictor/
|
|-- lstm_stock_prediction.ipynb        # Jupyter Notebook with full implementation
|-- model_visuals/                     # Charts of predictions and actual prices
|-- datasets/                          # (Optional) Exported stock data
|-- README.md                          # Project overview
```

---

## 📊 Evaluation Metric

- **RMSE (Root Mean Squared Error)**
- Helps evaluate how closely the model's predictions match real data.

---
