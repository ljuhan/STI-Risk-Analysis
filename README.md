# Financial Data Analysis: Straits Times Index (STI)

## 📌 Project Overview
A quantitative analysis tool designed to evaluate the historical performance and risk metrics of Singapore's blue-chip equities (Straits Times Index constituents). This project automates the extraction of financial data, calculates key risk indicators (volatility, correlation), and visualizes portfolio diversification potential.

## 🚀 Key Features
* **Automated Data Extraction:** Fetches adjusted close prices dynamically using `yfinance` API.
* **Risk Metrics Engine:** Calculates daily log returns, annualized volatility, and cumulative returns.
* **Correlation Analysis:** Generates heatmaps to identify diversification opportunities between STI constituents (e.g., DBS vs. Singtel).
* **Visualization:** Interactive time-series plotting and return distribution histograms.

## 🛠️ Technologies Used
* **Python 3.10+**
* **Pandas:** Time-series data manipulation.
* **NumPy:** Vectorized financial calculations.
* **Matplotlib / Seaborn:** Financial data visualization.
* **yfinance:** Market data retrieval.

## 📊 Methodology
1.  **Data Ingestion:** Downloads 5 years of historical data for selected tickers (e.g., `D05.SI`, `Z74.SI`, `O39.SI`).
2.  **Preprocessing:** Handles missing data points and adjusts for stock splits/dividends.
3.  **Statistical Analysis:**
    * *Daily Returns:* $R_t = \ln(\frac{P_t}{P_{t-1}})$
    * *Volatility:* Rolling standard deviation of returns.
    * *Correlation:* Pearson correlation coefficients to assess sector coupling.

## 💻 Getting Started

### Prerequisites
Ensure you have Python installed. It is recommended to use a virtual environment or Anaconda.

```bash
pip install pandas numpy matplotlib seaborn yfinance
