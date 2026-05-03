# Notebooks

The notebooks are organized by research stage. The cleaned GitHub-ready workflow is:

1. `01_statistical_validation/01_masi_return_statistical_investigation.ipynb`
2. `02_baseline_modeling/01_garch_var_es_benchmark_backtesting.ipynb`
3. `03_deep_learning_risk/01_lstm_var_es_hybrid_risk_modeling.ipynb`

Each notebook keeps result-producing cells visible for GitHub rendering. Reusable functions have been extracted into `../src/analysis/` to keep the notebooks focused on interpretation and outputs.

## Folder Map

- `01_statistical_validation/`: statistical diagnostics and return validation.
- `02_baseline_modeling/`: econometric baseline and benchmark modeling.
- `03_deep_learning_risk/`: deep-learning risk forecasting and hybrid VaR/ES experiments.
