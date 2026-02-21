# energy-risk-simulator
Quantitative risk modeling tool for electricity demand: forecasts loads using SARIMAX, simulates probabilistic scenarios via Monte Carlo, computes VaR, and recommends demand-response / hedging strategies. Built with real EIA hourly data.


A Python-based tool for quantitative risk modeling in electricity markets, using real historical demand data to forecast loads, simulate probabilistic scenarios, compute Value at Risk (VaR), and recommend risk management strategies.

Built as a portfolio project demonstrating skills relevant to quantitative risk roles in energy markets (e.g., demand-side resource strategies, statistical outcome weighting, risk hedging recommendations).

## Project Overview

This tool:
- Loads and cleans real hourly electricity demand & generation data from a U.S. Balancing Authority (Avista Corporation – AVA, via EIA/Kaggle dataset)
- Aggregates to daily level for stable modeling
- Forecasts future demand using SARIMAX (with seasonal patterns and exogenous drivers: temperature proxy + renewable share)
- Runs Monte Carlo simulations to generate thousands of possible demand paths and weight outcomes probabilistically
- Calculates 95% Value at Risk (VaR) for downside exposure
- Provides actionable risk management recommendations (e.g., when to activate demand-response or hedge positions)

## Key Features
- Real EIA data processing (hourly → daily aggregation)
- Time-series forecasting with seasonality (SARIMAX)
- Probabilistic risk simulation (Monte Carlo + normal-weighted averaging)
- Downside risk metrics (95% VaR)
- Rule-based strategy recommendations based on risk thresholds
- Visualizations (historical trends + forecast) and Excel report export

## Demo Outputs

### Demand Trend (2015–2021)
![Avista Daily Demand & Renewable Influence](ava_demand_trend.png)

### 90-Day Forecast Example
![Avista 90-day SARIMAX Forecast](ava_forecast.png)

### Recommended Risk Management Strategy:
Acceptable risk (VaR downside ~0.3%): Maintain current positioning; continue monitoring renewable variability and weather drivers.



# Sample Output Report
The tool generates an Excel report with cleaned data, forecast results, and risk metrics.

**Download the example report:**  
[ava_risk_report.xlsx](ava_risk_report.xlsx)
Contents:
- Cleaned_Data: Processed daily demand and drivers
- Forecast: Historical vs. forecasted demand
- Risk_Metrics: Monte Carlo weighted scenarios + 95% VaR for the 90-day horizon

