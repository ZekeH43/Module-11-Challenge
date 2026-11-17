# Forecasting Net Prophet

This is a preserved **FinTech course notebook**, updated with a project overview and basic source-integrity checks. The original assignment code remains in [forecasting_net_prophet.ipynb](forecasting_net_prophet.ipynb).

## Purpose

The exercise uses Python to demonstrate a historical time-series forecasting assignment with the Prophet forecasting toolkit. It is intended as a learning artifact and **has not been revalidated as a production or live-data application**.

## Repository layout

- Main notebook: `forecasting_net_prophet.ipynb`
- Source data: No separate source CSV is included in the current repository; inspect the notebook for its data-acquisition steps.
- `scripts/validate_assets.py`: built-in Python checks that notebooks are readable JSON and included CSV files have headers
- `.github/workflows/source-integrity.yml`: runs the source checks on pull requests

## Running locally

1. Use an isolated Python environment suitable for the historical notebook. Start with Python 3.10/3.11, adjusting packages as necessary.
2. From the repository root, optionally create a virtual environment:
   ```bash
   python -m venv .venv
   # Windows: .venv\Scripts\activate
   # macOS/Linux: source .venv/bin/activate
   python -m pip install notebook pandas matplotlib prophet hvplot
   ```
3. Launch Jupyter with the notebook directory as the working directory:
   ```bash
   cd .
   jupyter notebook forecasting_net_prophet.ipynb
   ```
4. Review the notebook's imports, file paths, package versions, and any external-data requirements before running cells in order.

The installation command is an **unverified starting point**, not a pinned or tested dependency set. Historic data formats and package APIs may need additional work.

## Lightweight repository validation

Run from the repository root:

```bash
python scripts/validate_assets.py
```

This checks file integrity only: it **does not execute notebooks, train models, test analytics, or validate numerical outcomes**.

## Limitations and portfolio context

Forecasts depend on the original dataset, notebook code, package compatibility, and any external data/API availability. Saved notebook outputs are not independently verified and should not be presented as current forecasts.

For an internship discussion, explain the data preparation, methods selected, evaluation limits, and what you would improve for reliable reproducibility. Original notebooks and assignment resources remain preserved.
