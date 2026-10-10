# Sales Forecasting with Prophet

A Google Colab-ready time-series forecasting project based on the **Synthetic Retail Sales** dataset. It uses daily sales for one store to explore patterns, compare a seasonal-naive baseline with Prophet, and forecast the next 30 days.

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
