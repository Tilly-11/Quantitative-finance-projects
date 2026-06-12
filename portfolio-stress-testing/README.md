# Macroeconomic Stress Testing & Scenario Analysis

This module features a functional risk-modeling framework designed to stress-test a multi-asset equity portfolio against systemic macroeconomic shocks and specific sector crises. Rather than analyzing daily normal volatility, this pipeline evaluates the portfolio's structural resilience against historical and hypothetical market dislocations.

## Evaluated Shock Scenarios
1. **The 2008 Lehman Brothers Collapse (Systemic Financial Panic)**: Simulates the single-day impact of September 29, 2008. Uses the S&P 500 (`^GSPC`) as a proxy model for assets that did not yet have active trading history during the Great Recession.
2. **The 2020 COVID-19 Liquidity Shock (Black Monday 2020)**: Replays the catastrophic market crash of March 16, 2020, where systemic liquidations caused a synchronized asset collapse across the entire economy.
3. **Hypothetical Tech Sector Meltdown**: Simulates a forward-looking concentration crisis, penalizing standard technology assets by -8% and placing a severe -15% structural penalty on high-beta growth equities (TSLA).

## Features & Modular Architecture
- **Proxy Modeling Engine**: Resolves the "asset lifespan problem" by automatically routing missing historical price series to index proxy benchmarks.
- **Mixed-Scenario Matrix Operations**: Uses vector dot products to instantly map multi-asset shock percentages to total budget drawdowns.
- **Automated Data Labeling Reporting**: Automatically calculates, places, and renders percentage and absolute dollar damage metrics onto saved reporting layouts.

## Code Structure
- `fetch_stress_data()`: Connects to market indices over a 17-year timeline to map historical stress registries.
- `run_scenario_analysis()`: Houses the logic for temporal historical extraction and hypothetical sector shocks.
- `plot_stress_results()`: Renders and crops localized bar charts displaying capital losses.
