# Bitcoin and Gold Price Prediction and Portfolio Maximization

This project explores the prediction of Bitcoin and Gold prices using ARIMA and LSTM models and develops tailored trading strategies to maximize portfolio profits. The study covers data preprocessing, price prediction modeling, and trading strategy implementation using benchmark and reinforcement learning methods.

## Authors
- Lexuan Zhu
- Qiancheng Ma
- Xinran Lin

---

## Problem Statement

The aim of this project is to:
1. Develop models using the past daily prices of Bitcoin and Gold (from 09/12/2016 to 08/09/2021) to predict the prices for the following month.
2. Create trading strategies to decide whether to buy, hold, or sell assets to maximize profits until 09/10/2021.

---

## Dataset

- **Source:** Daily prices of Bitcoin and Gold (09/12/2016 to 09/10/2021).
- **Preprocessing Steps:**
  - **Missing Values:** Filled using the average of the preceding and subsequent day prices.
  - **Weekend Prices:** Forward filled with Friday's prices for Gold.
  - **Train-Test Split:** Data before 08/10/2021 used for training; remaining data for testing.

---

## Methodology

### 1. Prediction
#### ARIMA (AutoRegressive Integrated Moving Average)
- **Key Steps:**
  - Explored the stationarity and seasonality of data.
  - Selected ARIMA models based on lowest AIC values.
  - Updated models iteratively with observed prices.
- **Results:**
  - ARIMA(2,1,2) for Gold, ARIMA(1,1,1) for Bitcoin showed good performance.

#### LSTM (Long Short-Term Memory Neural Networks)
- **Architecture:**
  - 3 LSTM layers followed by a Dense layer.
  - Captures long-term dependencies in time-series data.
- **Results:**
  - Successfully modeled and predicted trends for both assets.

---

### 2. Trading Strategies
#### Reinforcement Learning (Deep Q-Learning)
- **Approach:**
  - Utilized a neural network to approximate Q-values and train trading policies based on the Bellman equation.
- **Performance:**
  - For Bitcoin: RL achieved ~1-2% profitability, outperforming benchmark strategies.
  - For Gold: RL underperformed due to market stability favoring simpler strategies.

#### Benchmark Strategies
- **Compared Results:**
  - Static strategies performed better for Gold due to price stability.
  - Dynamic RL strategies excelled in Bitcoin trading due to market volatility.

---

## Conclusion

- **Bitcoin:** RL-based strategies demonstrated superior adaptability and profitability in volatile markets.
- **Gold:** Simpler, static trading strategies performed better due to market stability.

---

## References

1. Liu, F., Li, Y., Li, B., Li, J., & Xie, H. (2021). Bitcoin transaction strategy construction based on deep reinforcement learning. *Applied Soft Computing, 113*, 107952. [DOI Link](https://doi.org/10.1016/j.asoc.2021.107952)

---

## Acknowledgments

This project was developed as part of the Mathematical Contest in Modeling (MCM-C). Learn more: [MCM-C 2022](https://www.mathmodels.org/Problems/2022/MCM-C/index.html).

---
