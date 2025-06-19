# Investing_Stocks_Strategy
This project involves a detailed analysis of stock investment strategies using Python. Historical stock data of 9 companies from 3 sectors was scraped from Yahoo Finance. Buy & Hold and Momentum Trading were implemented and compared against the S&P 500 index. Monte Carlo simulations and mean variance optimization (using Pyomo) were employed to assess risk return profiles and identify the optimal portfolio allocation. Results showed that while strategy performance varied across stocks, the S&P 500 index yielded the highest overall return during the selected period.

## Objective

To simulate and compare the performance of:
- Buy & Hold Strategy**
- Momentum Trading Strategy**
- S&P 500 Index Benchmark**

and determine which strategy yields the highest return under controlled risk constraints.

## Companies Selected (3 from each sector)

- Consumer Sector: Nike (NKE), Tapestry Inc. (TPR), McDonald's (MCD)  
- Technology Sector: Intel (INTC), Autodesk (ADSK), Verisk (VRSK)  
- Industrial Sector: Caterpillar (CAT), Honeywell (HON), Fidelity Information Services (FIS)

## Data Collection

- Data Source: [Yahoo Finance](https://finance.yahoo.com/)
- Time Period: 2017-01-01 to 2022-11-02
- Collected data: Daily and Monthly prices
- Libraries used: `yahoo_fin`, `pandas`, `numpy`, `matplotlib`, `pyomo`

## Methodology

### 1. Data Scraping
- Downloaded 5 years of stock data for 9 companies.
- Pulled both daily and monthly historical prices.

### 2. Strategy Implementation

- Buy & Hold: Invest fixed capital and hold till end date.
- Momentum Strategy: Buy/sell based on moving average crossovers (9-day vs 21-day).
- S&P 500 Index: Used as a benchmark for performance comparison.

### 3. Portfolio Optimization
- Applied **Mean-Variance Optimization** using Pyomo to identify the best portfolio allocation under risk constraints.
- Used binary constraints to select one stock from each sector.
- Evaluated system return based on different risk levels.

## Results

| Strategy                   | Final Value (Nov 2022) |
|---------------------------|------------------------|
| Buy & Hold Strategy       | $93,253                |
| Momentum Trading Strategy | $88,033                |
| S&P 500 Benchmark         | $105,375               |

- S&P 500 Index** outperformed both strategies.
- For individual stocks:
  - Verisk → Momentum was better.
  - Autodesk & McDonald's → Buy & Hold performed better.

## Key Takeaways

- Optimal investment strategy depends on stock characteristics and market behavior.
- Risk-return analysis plays a vital role in portfolio construction.
- Strategy effectiveness varies across different stocks and time periods.
- S&P 500 is a strong benchmark that performed better in this period.

## Tools & Libraries

- Python
- Jupyter Notebook
- `yfinance`
- `pyomo` for optimization modeling
- `matplotlib`, `seaborn` for plotting
