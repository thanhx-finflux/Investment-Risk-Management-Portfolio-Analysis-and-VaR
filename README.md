# Investment-Risk-Management-Portfolio-Analysis-and-VaR
Python-based analysis of MAANG portfolio (APPL, AMZN, GOOGL, META, NFLX) plus S&amp;P 500 using yfinance data, calculating returns, volatility, correlations, beta, CAPM, portfolio optimization, and Value at Risk (VaR).


## Overview

This project demonstrates quantitative risk management:
- Fetches historical prices.
- Calculates metrics for individual stocks and portfolios.
- Optimizes weights for minimum variance.
- Estimates VaR using historical simulation.

## Key Calculations
- Daily Returns: Log return for accuracy.
- Volatility: Annualized standard deviation.
- Correlations: Pairwise heatmap.
- Beta and CAPM: Vs. S&P 500, expected returns formula.
- Portfolio Optimization: Minimum variance using covariance.
- VaR: 95% 99% confidence via sorted returns.

## Requirements:
    - yfinance
    - pandas
    - numpy
    - matplotlib

```python
# Fetch historical market data for FB, AAPL, AMZN, NFLX, GOOGL, S&P 500
start_date = "2020-01-01"
end_date = datetime.today().strftime('%Y-%m-%d')
close_price = yf.download("META AAPL AMZN NFLX GOOGL ^GSPC", start=start_date, end=end_date, auto_adjust=True)['Close']
close_price
```

## Results
- Volatility: LFLX highest
- Beta: MAANG stock > 1 (high market sensitivity)
- Portfolio VaR: 95% - 15.6%, 99% - 26.6%
- Optimized weights: Balances risk (lower NFLX allocation)

# Visualizations:

Daily return heatmap

<img width="774" height="699" alt="Image" src="https://github.com/user-attachments/assets/21c5e3fb-12af-494d-8906-39810911efd4" />

VaR Bar Plot

<img width="878" height="545" alt="Image" src="https://github.com/user-attachments/assets/eeeb69e1-359c-48c0-93b7-4733fe7fa849" />

## Contact
Thanh Xuyen, Nguyen
- LinkedIn: [xuyen-thanh-nguyen-0518](https://www.linkedin.com/in/xuyen-thanh-nguyen-0518/)
- Email: thanhxuyen.nguyen@outlook.com
