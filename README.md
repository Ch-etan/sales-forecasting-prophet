# Sales Forecasting with Prophet

A Google Colab-ready time-series forecasting project based on the **Synthetic Retail Sales** dataset. It uses daily sales for one store to explore patterns, compare a seasonal-naive baseline with Prophet, and forecast the next 30 days.

## Open in Google Colab

Replace `YOUR_GITHUB_USERNAME` with your GitHub username:

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/YOUR_GITHUB_USERNAME/sales-forecasting-prophet/blob/main/sales_forecasting_prophet.ipynb)

## Dataset

The CSV contains `date`, `store`, and `sales` columns and is available from the [dataset source on GitHub](https://github.com/shibilasherinn/Retail-Sales-Forecasting/blob/main/retail_sales_synthetic.csv).

The notebook loads the dataset directly from the public raw CSV by default. To use a downloaded copy, set `LOAD_FROM_URL = False` and upload the CSV when prompted.

## Methods

- Exploratory data analysis: sales trend, weekday distributions, monthly seasonality
- Daily calendar with explicit handling of missing dates/sales
- Chronological holdout: final 84 calendar days
- Baseline: latest training sales value for each weekday
- Forecast model: Prophet with weekly and yearly seasonality
- Metrics: MAE, RMSE, WAPE
- Outputs: actual vs. holdout forecast and next-30-day forecast

## Run it

1. Open the notebook using the Colab badge above.
2. Run the cells from top to bottom.
3. The dataset loads directly by default; upload your local CSV if you switch `LOAD_FROM_URL` to `False`.
4. Review the evaluation table and plots.
5. Record your **actual** model metrics and findings below.

## Results and findings

Fill this section in after running the notebook. Do not publish fabricated metrics.

- Store analyzed:
- Best model on test dates:
- MAE:
- RMSE:
- WAPE:
- Weekly/yearly patterns:
- Forecast limitations and next steps:

## Promotion and feature limitations

This dataset contains only date, store, and sales. It does **not** include promotions, prices, or a holiday calendar. The notebook therefore models trend and seasonality but does not claim to measure promotional effects. Add a real promotion calendar as an extra regressor only if reliable historical and future promotion values are available.

## Important notes

- The test split is chronological; rows are not randomly shuffled.
- Missing values in the training period are imputed using training data only for the holdout evaluation.
- Test dates without observed sales are excluded from metric calculations.
- The dataset is synthetic, so results may not represent real retail demand.
- Do not commit a raw data file to a public repository unless its terms permit redistribution.

## Project structure

```text
sales-forecasting-prophet/
├── sales_forecasting_prophet.ipynb
├── README.md
├── .gitignore
└── LICENSE
```
