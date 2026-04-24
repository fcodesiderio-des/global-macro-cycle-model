# global-macro-cycle-model
# Global Macroeconomic Cycle Model

This project builds a reproducible Python pipeline for public macroeconomic and market data. It fetches raw observations, aligns them to month-end frequency, computes macro-cycle indicators and category scores, classifies each month into an economic regime, and produces an interactive Plotly dashboard.

## What It Creates

- Source-specific fetch scripts:
  - `scripts/fetch_fred.py`
  - `scripts/fetch_worldbank.py`
  - `scripts/fetch_imf.py`
  - `scripts/fetch_oecd.py`
  - `scripts/fetch_bis.py`
  - `scripts/fetch_yfinance.py`
- Raw source files in `data/raw/<source>/`
- A unified monthly long-form dataset at `data/processed/monthly_dataset.csv`
- Category and final model outputs:
  - `data/processed/category_scores.csv`
  - `data/processed/macro_scores.csv`
- A Plotly dashboard at `dashboards/macro_cycle_dashboard.html`

## Setup

```bash
python3 -m venv .venv
source .venv/bin/activate
pip install -r requirements.txt
cp .env.example .env
```

Add your free FRED API key to `.env`:

```bash
FRED_API_KEY=your_key_here
```

## Run The Pipeline

Fetch all available sources, process, score, and build the dashboard:

```bash
python3 scripts/run_pipeline.py
```

Use existing raw data and rebuild only the model outputs:

```bash
python3 scripts/run_pipeline.py --skip-fetch
```

Fetch selected sources:

```bash
python3 scripts/run_pipeline.py --sources fred yfinance worldbank
```

Run individual stages:

```bash
python3 scripts/fetch_fred.py
python3 scripts/fetch_worldbank.py
python3 scripts/fetch_imf.py
python3 scripts/fetch_oecd.py
python3 scripts/fetch_bis.py
python3 scripts/fetch_yfinance.py
python3 scripts/build_dataset.py
python3 scripts/score_model.py
python3 scripts/build_dashboard.py
```

## Configuration

Edit `config/indicators.yaml` to change:

- Source indicators and tickers
- Countries
- Transformation type (`level`, `yoy`, `log_yoy`, `diff_yoy`)
- Direction of each indicator, where `1` means higher is better for the cycle and `-1` means higher is worse
- Category weights for the final score

The final score is a weighted combination of:

- Growth
- Inflation
- Policy/liquidity
- Labor
- Financial stress
- Market momentum

## Data Sources

The project is designed for free public sources first:

- FRED for U.S. macro, rates, yield curves, credit spreads, VIX, money supply, and financial stress
- World Bank for country-level GDP, inflation, unemployment, trade, and debt indicators
- IMF DataMapper for WEO-style growth, inflation, debt, and fiscal balance series
- OECD for Composite Leading Indicators
- BIS for policy rates, credit-to-GDP, debt service ratios, and liquidity series when public CSV URLs are configured
- Yahoo Finance through `yfinance` for market indicators such as ACWI, SPY, EEM, HYG, LQD, TLT, GLD, DBC, and VIX

The BIS portal has multiple dataflows and key structures, so `scripts/fetch_bis.py` supports direct CSV URLs added to `config/indicators.yaml`. This keeps the pipeline reproducible once a specific BIS dataset and country coverage are chosen.

## Transformation Logic

The processed monthly dataset contains:

- `date`
- `indicator_name`
- `source`
- `category`
- `frequency`
- `value`
- `transformed_value`
- `z_score`
- `momentum_3m`
- `momentum_6m`

Transformation rules:

- Level indicators such as rates, spreads, unemployment, CLI, PMI-like indexes, and stress indexes are kept as levels.
- Level-growth indicators such as CPI, money supply, industrial production, trade, and market indexes use year-over-year growth.
- Daily, weekly, and monthly data are aligned to month end using the last available observation.
- Quarterly and annual observations are forward-filled to monthly frequency while preserving the original `frequency` metadata.
- Momentum is the 3-month or 6-month change in the transformed value.
- Rolling z-scores use a 240-month window when available.
- If fewer than 240 months are available, the model uses available history and sets `limited_history_flag`.

## Regime Classifier

Each month is classified as one of:

- Early expansion
- Mid expansion
- Late expansion
- Slowdown
- Recession
- Recovery

The classifier uses interpretable rules based on growth level, growth momentum, inflation trend, policy/liquidity stance, labor trend, credit stress, and market momentum. The rules are intentionally transparent so they can be audited and adjusted as the model matures.

## Dashboard

The Plotly dashboard shows:

- Current regime and latest macro-cycle score
- Historical macro-cycle curve
- Indicator heatmap
- Latest readings table
- Weighted contribution by category
- Historical score comparison across recession, expansion, slowdown, and recovery regimes

Open:

```bash
dashboards/macro_cycle_dashboard.html
```

## Validation

Run the included smoke test:

```bash
python3 tests/test_processing.py
```

It verifies monthly alignment, transformations, category scoring, final score bounds, and regime output on synthetic data.

## Limitations

- Public macro data are released with lags and may be revised after first publication.
- Country coverage is uneven across World Bank, IMF, OECD, and BIS sources.
- Annual and quarterly data are forward-filled to monthly frequency, which improves alignment but does not create new information.
- Rolling z-scores are less stable when less than 20 years of history are available. These rows are flagged.
- Market data from Yahoo Finance can differ from official vendor data due to adjustments, ticker availability, and licensing constraints.
- The regime classifier is a transparent rules engine, not a causal model. It should be reviewed before being used for investment, policy, or risk decisions.
- Category weights are configurable but subjective. Sensitivity testing is recommended before relying on the final score.
