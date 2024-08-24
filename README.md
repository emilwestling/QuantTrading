# QuantTrading

## Overview

This project is developed under mentorship of Dr. Fahad Sultan. Dr. Sultan is a professor in computer science at Furman University and we conducted this project as a half-year research project. The project focuses on analyzing and predicting the stock prices of the top 150 companies by dollar volume in the S&P 500 index using LSTM (Long Short-Term Memory) models. The model predicts stock prices and optimizes a portfolio based on these predictions.

**Key features of this project include**:

- Data extraction and preprocessing from Yahoo Finance.
- Implementation of LSTM models for stock price prediction.
- Optimization of portfolio weights using the Efficient Frontier.
- Performance evaluation against SPY (S&P 500 ETF) and visualization of returns.

## Data Collection

- **Yahoo Finance**: Historical stock data for all companies in the S&P 500 index from 2000-01-01 to 2024-02-19.

## Models Used

### LSTM

- **Price Prediction**: Predicts the stock price using historical stock data, adjusting for relevant time-series patterns.
- **Portfolio Optimization**: Optimizes a portfolio based on predicted stock prices using the Sharpe ratio as the primary metric.

## Trading Strategy

**The trading strategy developed can be broken down in these steps**:

- **LSTM Predictions** Use the Long-Short Term Memory model to predict the stock price of the each stock at the end of the following month.
- **Top 15 Stocks** Pick out the top 15 best performing stocks for the following month. If there aren't 15 stocks with positve returns, only pick the ones with predicted positive returns.
- **Optimize Weights** Optimize the weights for the portfolio based on the sharpe ratio. I.e. maximize the sharpe ratio for the portfolio.
- **Repeat**: Repeat for each month.

## Results

![Portfolio Performance](images/portfolio_performance.png)

## How to Run the Code

1. **Clone the Repository**:

   ```bash
   git clone https://github.com/emilwestling/QuantTrading.git
   cd QuantTrading
   ```

2. **Install Dependencies**:

   ```bash
   pip install -r requirements.txt
   ```

3. **Run the Jupyter Notebook**:
   - Open the notebook `LSTM_Portfolio.ipynb` in Jupyter Notebook or JupyterLab.

## Repository Structure

- `index.html`: Portfolio website.
- `LSTM_Portfolio.ipynb`: Jupyter Notebook containing the project code and analysis.
- `images/`: Directory containing result chart.
- `requirements.txt`: File listing the necessary Python packages for the project.

## Project Repository

You can find the full code and data on my [GitHub repository](https://github.com/emilwestling/QuantTrading).

## Conclusion

We managed to generate a trading strategy that outperforms the S&P 500 index substainally. I would like to express my gratitude to Professor Sultan for his guidance.

## License

This project is licensed under the MIT License. See the [LICENSE](LICENSE) file for details.

## Contact

If you have any questions or feedback, please contact me at [westling01@gmail.com](mailto:westling01@gmail.com).
