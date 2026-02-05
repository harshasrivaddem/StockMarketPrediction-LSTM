# 📈 MRF Stock Price Prediction using LSTM

## 📌 Project Overview
This project focuses on **time series forecasting** to predict the **closing stock price of MRF Limited** using a **Long Short-Term Memory (LSTM)** neural network.

The model is trained on **5 years of historical stock data** (from **30 August 2018 to 30 August 2023**) using OHLCV (Open, High, Low, Close, Volume) information.  
LSTM is used because of its effectiveness in capturing long-term dependencies in sequential data such as stock prices.

---

## 📊 Dataset Description
- Source: Yahoo Finance  
- Stock: **MRF Limited (MRF.NS)**  
- Time Period: **Aug 2018 – Aug 2023**
- Total Records: **1234**
- Features:
  - Date
  - Open
  - High
  - Low
  - Close
  - Volume

> Dataset link:  
> https://finance.yahoo.com/quote/MRF.NS/history?p=MRF.NS

---

## 🛠️ Tools & Libraries Used
- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- TensorFlow / Keras
- Scikit-learn

---

## 🔍 Exploratory Data Analysis (EDA)
- Converted `Date` column to datetime format
- Analyzed statistical summary of numerical features
- Removed redundant `Adj Close` column
- Verified absence of missing values
- Visualized:
  - Feature distributions
  - Box plots for outlier detection
  - Stock price trends over time
  - Open vs Close prices
  - Trading volume
  - Correlation heatmap

---

## 🔄 Data Preprocessing
- Selected **Close price** for prediction
- Applied **MinMax Scaling** to normalize data
- Used **95% data for training**, remaining **5% for testing**
- Created sequences of **60 days** to predict the next day’s price
- Reshaped data for LSTM input format

---

## 🤖 Model Architecture
- **Model Type:** Sequential LSTM
- Layers:
  - LSTM (64 units, return sequences)
  - LSTM (64 units)
  - Dense (32 units)
  - Dropout (0.5)
  - Dense (1 output unit)
- Optimizer: Adam
- Loss Function: Mean Squared Error (MSE)
- Epochs: 10

---

## 📈 Model Performance
Evaluation metrics on test data:

- **Mean Squared Error (MSE):** `15,949,853`
- **Root Mean Squared Error (RMSE):** `3993.73`

These results indicate that the model is able to capture the overall trend of the stock price effectively.

---

## 📊 Results & Visualization
- The predicted stock prices closely follow the actual closing prices
- The prediction curve shows an **upward trend**, consistent with historical movement
- The green line in the final plot represents **predicted closing prices**


