# Mean Reversion - Pairs Trading Strategy

## Introduction
Mean reversion is a popular trading strategy in finance, particularly in pairs trading. This strategy involves identifying two assets that move similarly with each other and exploiting deviations from their typical relationship. Pairs trading aims to capitalize on the convergence of the prices of two correlated assets after they deviate from their historical relationship.

## Basic Idea
1. **Identification of Pairs**: Find two assets with a high correlation (> 0.8) between their prices.
2. **Long and Short Positions**: Establish long positions in the undervalued asset and short positions in the overvalued asset.
3. **Trading Signal**: Use signals such as the Price Ratio to trigger trades when the ratio deviates significantly from its historical mean, typically measured using standard deviation.

## Implementation
- The project utilizes historical stock price data for PepsiCo (PEP) and The Coca-Cola Company (KO) for the year 2014.
- Historical price data is obtained using Yahoo Finance API through the `pandas_datareader` library.
- The correlation between PEP and KO prices is analyzed using statistical methods like Pearson correlation coefficient and cointegration tests.
- Trade signals are generated based on deviations from the historical mean of the Price Ratio (PEP/KO).
- Sentiment analysis data for both PepsiCo and Coca-Cola tweets in 2014 are incorporated to adjust trade sizes based on sentiment.
  
## Results
- The strategy's profitability is evaluated based on Mark-to-Market (MTM) daily profit/loss, daily returns, and Sharpe ratio.
- The project also assesses drawdowns and cumulative returns to provide insights into risk management and performance evaluation.

## Directory Structure
- `sentiment_analysis.py`: Python script for sentiment analysis and trade scaling.
- `pepsi_tweets_data.csv`: Sentiment analysis data for PepsiCo tweets in 2014.
- `coke_tweets_data.csv`: Sentiment analysis data for Coca-Cola tweets in 2014.

## Requirements
- Python 3.x
- pandas
- pandas_datareader
- yfinance
- numpy
- seaborn
- statsmodels
- matplotlib

## How to Run
1. Clone the repository.
2. Install the required libraries using `pip install -r requirements.txt`.
3. Run `main.py` to execute the pairs trading strategy.

