# Investments Project - Building an optimal portfolio of assets

## Overview

This project aims to build and analyze optimal investment portfolios using various financial signals. The primary focus is on combining beta, idiosyncratic volatility, and momentum signals to construct and evaluate different investment strategies. The project involves downloading and processing historical stock data, constructing portfolios, and analyzing their performance against standard risk factors.

Please look at our implementation [here](FinalNotebook.ipynb).
## Project Goals

### Data Collection and Preparation
- **Download Historical Data**: 
  - Monthly stock returns from CRSP for NYSE and AMEX from January 1, 1964, to December 31, 2023.
  - Value-weighted CRSP market returns and 1-month T-bill returns as the risk-free rate.

### Betting Against Beta (BaB) Strategy
- Compute time-varying market beta for each stock using rolling 5-year regressions.
- Sort stocks into deciles based on beta and compute returns for decile portfolios.
- Construct the BaB factor and analyze its performance.

### Momentum Strategy (Mom)
- Construct a long-short momentum strategy by sorting stocks into deciles based on their 1-month lagged 11-month return.
- Compute returns for decile portfolios and analyze the momentum strategy's performance.

### Idiosyncratic Volatility (IV) Strategy
- Estimate each stock’s idiosyncratic volatility using rolling 5-year regressions.
- Sort stocks into deciles based on idiosyncratic volatility and compute returns for decile portfolios.
- Construct the IV factor and analyze its performance.

### Optimal Fund Portfolio Return (STRAT)
- Combine BaB, IV, and Mom strategies to create an optimal fund portfolio targeting an average annual volatility of 10%.
- Evaluate different approaches to combine the strategies: equal weight, risk-parity, and mean-variance optimization.

### Performance and Risk Analysis
- Regress the strategy returns on industry portfolio returns and Fama-French 5 research factors.
- Analyze the exposure of the strategy to market and industry risks.
- Construct an industry-hedged STRAT portfolio and compare its performance.

### Industry Neutral Strategy
- Build industry-neutral portfolios by constructing BaB, IV, and Mom strategies separately for each industry.
- Combine these industry-specific strategies to create a new industry-neutral STRAT.
- Compare the performance of the industry-neutral STRAT with the original and hedged STRAT portfolios.

