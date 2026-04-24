Build a Python project that creates a global macroeconomic cycle model.

Objective:
Create a reproducible system that fetches public macroeconomic and market data, transforms it into a unified monthly dataset, computes macro-cycle scores, classifies the current economic regime, and produces a Plotly dashboard.

Use free public data sources first:
- FRED API for U.S. macro, rates, yield curves, credit spreads, VIX, money supply, and financial stress.
- World Bank API for global and country-level GDP, inflation, unemployment, trade, and debt indicators.
- IMF DataMapper or IMF SDMX API for WEO forecasts: GDP growth, inflation, government debt, fiscal balance.
- OECD API for Composite Leading Indicators.
- BIS Data Portal or BIS bulk downloads for credit-to-GDP, debt service ratios, central bank policy rates, and global liquidity.
- Yahoo Finance through yfinance for market indicators: ACWI, SPY, EEM, HYG, LQD, TLT, GLD, DBC, VIX.

Create:
1. A data-fetching layer with one script per source:
   - fetch_fred.py
   - fetch_worldbank.py
   - fetch_imf.py
   - fetch_oecd.py
   - fetch_bis.py
   - fetch_yfinance.py

2. A unified monthly time-series dataset:
   - Align all indicators to month-end frequency.
   - Convert quarterly series to monthly using forward-fill, but preserve original frequency metadata.
   - Store raw and processed data separately.
   - Include columns for date, indicator_name, source, category, frequency, value, transformed_value, z_score, momentum_3m, momentum_6m.

3. Transformations:
   - YoY growth for level indicators such as CPI, money supply, industrial production, trade, and market indexes.
   - Level values for rates, spreads, unemployment, PMI, CLI, and financial stress indexes.
   - 3-month and 6-month momentum measures.
   - Rolling z-scores using a 20-year window when possible.
   - If 20 years of history are unavailable, use all available history and flag the limitation.

4. Category scores:
   - Growth score
   - Inflation score
   - Policy/liquidity score
   - Labor score
   - Financial stress score
   - Market momentum score

5. Final macro-cycle score:
   - Normalize category scores.
   - Combine them into a score from -100 to +100.
   - Make category weights configurable in a YAML or JSON config file.

6. Regime classifier:
   Classify each month into one of:
   - Early expansion
   - Mid expansion
   - Late expansion
   - Slowdown
   - Recession
   - Recovery

   The classifier should use:
   - Growth level
   - Growth momentum
   - Inflation trend
   - Policy stance
   - Labor trend
   - Credit stress
   - Market momentum

7. Dashboard:
   Build a Plotly dashboard showing:
   - Current regime
   - Historical macro-cycle curve
   - Indicator heatmap
   - Latest readings table
   - Contribution by category
   - Historical comparison versus prior recessions and expansions

8. Documentation:
   - Create README.md with setup instructions.
   - Create .env.example for API keys.
   - Create requirements.txt.
   - Add comments explaining each transformation and scoring step.
   - Include a limitations section explaining data lags, missing data, and model risk.

Use:
- pandas
- numpy
- fredapi
- wbgapi
- requests
- yfinance
- scikit-learn
- statsmodels
- plotly
- pyyaml

Make the code modular, reproducible, and documented.
