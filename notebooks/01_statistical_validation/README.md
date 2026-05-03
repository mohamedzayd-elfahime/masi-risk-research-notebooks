# Statistical Validation Notebooks

This folder contains notebooks used to validate the MASI dataset before risk modeling.

## Recommended Order

1. `01_masi_return_statistical_investigation.ipynb`
   - Statistical characterization of MASI returns.
   - Covers log returns, distribution diagnostics, stationarity tests, volatility clustering, ARCH-LM, Ljung-Box, and leverage asymmetry.

The deep-learning notebook was moved to `../03_deep_learning_risk/` because it trains and evaluates the LSTM VaR plus Ridge ES workflow rather than only validating statistical properties.
