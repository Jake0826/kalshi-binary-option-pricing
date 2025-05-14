# Kalshi Binary Option Pricing

![Sample Analysis](sample.png)

This repository contains code and data for analyzing and pricing binary options on the S&P 500 closing price using Kalshi's prediction market. I developed a model capable of predicting option pricing with an R-squared value consistently above 0.8.

## Research Summary

This project examines the pricing dynamics of binary options on Kalshi's prediction market platform, focusing on S&P 500 year-end closing value contracts. The research investigates:

1. The relationship between theoretical models and actual market prices
2. How effectively adapted Black-Scholes models predict binary option prices
3. Potential trading opportunities from identified mispricings

The analysis focuses on two types of contracts:
- "Above" contracts (e.g., "Will the S&P 500 be above 5799.99 at the end of Dec 31, 2024?")
- "Between" contracts (e.g., "Will the S&P 500 be between 4500 and 4699.99 at the end of Dec 29, 2023?")

Key findings:
- The adapted Black-Scholes model shows strong predictive power for "above" contracts (R > 0.9) 
- Strong autocorrelation patterns suggesting predictable price movements

The research utilizes three primary data sources:
- S&P 500 closing prices from NASDAQ
- Kalshi trade history
- Interest rate data from FRED

## File Structure

- **Notebooks**:
  - `kalshi.ipynb`: Analysis of Kalshi data
  - `sp500.ipynb`: Analysis of S&P 500 data 
  - `exploration.ipynb`: Data exploration and analysis of the relationship between Kalshi Option Prices and the S&P500 underlying  

- **Data Files**:
  - `data/sp500.csv`: Historical S&P 500 price data
  - `data/r.csv`: Risk-free rate data for pricing calculations
  - `data/kalshi_trades.csv`: Historical trading data from Kalshi platform

- **API Client**:
  - `KalshiClientsBaseV2ApiKey.py`: Implementation of the Kalshi API client for data retrieval

- **Report**:
  - `Binary_Option_Pricing.pdf`: A 4-page report summarizing the research findings, methodology, and key insights from the analysis.


## Getting Started

1. Ensure you have Python installed with Jupyter notebook support
2. Input your Kalshi API key in `kalshi.ipynb`
3. Open the notebooks in Jupyter to begin analysis
