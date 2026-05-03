# Dynamic Extreme Risk Management Framework for the MASI Index

This repository develops an adaptive downside-risk framework for the Moroccan MASI index. The workflow starts with statistical validation of return behavior, compares econometric VaR/ES benchmarks, then explores hybrid deep-learning and regime-aware risk models for dynamic exposure control.

## Repository Structure

- `data/processed/`: processed and transformed datasets used by the notebooks.
- `notebooks/`: research notebooks organized by analysis stage.
- `src/analysis/`: reusable functions extracted from the notebooks for cleaner GitHub review.
- `.github/workflows/`: lightweight GitHub Actions checks.

For the dashboard application, see the companion repository:
`masi-risk-forecasting-dashboard`.

## Essential Notebooks

Read these notebooks first:

1. `notebooks/01_statistical_validation/01_masi_return_statistical_investigation.ipynb`
   - Validates MASI return properties: log returns, normality, stationarity, volatility clustering, ARCH effects, and leverage asymmetry.
2. `notebooks/02_baseline_modeling/01_garch_var_es_benchmark_backtesting.ipynb`
   - Builds EGARCH and GJR-GARCH benchmark forecasts, then runs statistical and economic backtests.
3. `notebooks/03_deep_learning_risk/01_lstm_var_es_hybrid_risk_modeling.ipynb`
   - Studies candidate predictors and evaluates the hybrid LSTM VaR plus Ridge ES workflow.

## Reusable Analysis Modules

The most important notebook functions were moved into:

- `src/analysis/garch_benchmark_utils.py`
- `src/analysis/risk_backtesting.py`
- `src/analysis/economic_evaluation.py`
- `src/analysis/lstm_var_es_pipeline.py`

The notebooks keep the narrative, plots, tables, and final execution cells. The modules keep reusable code separated so the project is easier to review and maintain.

## Setup

```bash
pip install -r requirements.txt
```

Then open the notebooks from the repository root so relative data paths resolve correctly.

## Data Files

The notebooks read the CSV files directly:

- `data/processed/final/master_dataset.csv`
- `data/processed/transformed/masi_transformed.csv`

Excel versions are also included for manual inspection:

- `data/processed/final/master_dataset.xlsx`
- `data/processed/transformed/masi_transformed.xlsx`

## License

This repository is source-available for review and demonstration only. All
rights are reserved.

Using, modifying, publishing, forking publicly, redistributing, commercializing,
or presenting this project in another portfolio, CV, GitHub profile, website,
school submission, demo, or public showcase is not permitted without prior
written permission.

If written permission is granted for reuse, attribution to the original author
and original MASI risk notebooks project must be preserved. See [LICENSE](LICENSE).
