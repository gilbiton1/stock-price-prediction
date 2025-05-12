# 📈 Stock Price Prediction – Hybrid ML + Time Series Similarity

This project explores a hybrid approach to short-term stock direction forecasting using both machine learning and time-series similarity techniques.

## 📌 Project Overview
We developed a prediction framework:
-  **sequence similarity model** using Dynamic Time Warping (DTW) and SAX symbolic transformation to identify short-term temporal patterns.
This model are combined in a hybrid prediction strategy that balances local sequence trends and global feature-based learning.
## 📁 Dataset
- **Source**: Yahoo Finance – 5 years of daily stock data from the S&P 500 index
- **Target stock**: AAPL (Apple Inc.)
- Features include OHLC prices, volume, and technical indicators (MACD, RSI, Bollinger Bands)
## ⚙️ Methodology
1. **Feature Engineering**:
   - Extracted PROC (Price Rate of Change) windows
   - Calculated technical indicators
   - Applied SAX for dimensionality reduction
2. **Modeling Pipeline**:
   - **Baseline**: XGBoost classifier on AAPL data
   - **Multi-stock Extension**: Selected top 5 co-integrated stocks (via Engle-Granger test)
   - **Sequence Similarity**: Used DTW to find similar price movement patterns
   - **Hybrid Model**: Combined predictions from both methods with weighted averaging
## 📊 Results & Insights
The hybrid model consistently outperformed single-method approaches by leveraging both structural relationships across stocks and temporal alignment within each stock's history.

---
## 📂 Files
- `Stock Price Prediction.ipynb` – Full code notebook  
- `Stock Price Prediction Presentation.pptx` – Project summary presentation  
- `Stock_Prediction_using_adavanced_time_series_similarity_paper.pdf` – Technical paper with detailed methodology
---
