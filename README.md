# Red Wine Demand Forecasting: Time Series Analysis

## Project Overview

This project analyzes monthly red wine demand using time series analysis techniques in Python.

The dataset covers the period from 1980 to 1995. The initial analysis focuses on preparing the time series data, establishing a monthly datetime index, and visualizing historical demand patterns.

The project is designed to provide a foundation for demand forecasting using statistical time series models and forecasting evaluation metrics.

## Business Objectives

- Explore historical monthly red wine demand.
- Identify potential trends and seasonal patterns.
- Prepare the dataset for time series modeling.
- Explore forecasting approaches such as ARIMA, Exponential Smoothing, and Prophet.
- Evaluate forecasting accuracy using appropriate error metrics.
- Generate insights that could support demand planning and inventory management.

## Dataset

**Dataset file:** `Red_Wine.csv`

The notebook uses the following source columns:

- `YEAR` — Year of observation.
- `MONTH` — Month of observation.
- `RED WINE` — Recorded red wine demand.

The `RED WINE` column is renamed to `demand`, while the year and month fields are combined into a monthly datetime index.

**Observation period:** 1980–1995.

The exact number of observations, demand units, and missing-value status should be verified during data validation.

## Tools & Technologies

- **Python** — Data processing and analysis
- **Pandas** — Data manipulation and time series preparation
- **NumPy** — Numerical operations
- **Matplotlib** — Time series visualization
- **Statsmodels** — Seasonal decomposition, ARIMA, and Exponential Smoothing
- **Prophet** — Forecasting model exploration
- **Scikit-learn** — Forecast evaluation metrics
- **Jupyter Notebook / Google Colab** — Interactive analysis

## Methodology

### 1. Data Loading and Preparation

The notebook loads the red wine dataset and renames the demand column for easier analysis.

### 2. Date Conversion

The `YEAR` and `MONTH` columns are combined into a datetime column using the `%Y-%B` format.

This creates a chronological monthly date index.

### 3. Time Series Formatting

The dataset is sorted chronologically, reduced to the date and demand columns, and indexed by date.

The frequency is set to month-start (`MS`) to establish a regular monthly time series.

### 4. Exploratory Time Series Visualization

A line chart is created to visualize monthly red wine demand over time.

This helps examine historical fluctuations and identify potential trends or recurring patterns.

### 5. Forecasting Models to Explore

The notebook imports libraries for the following forecasting approaches:

- **ARIMA:** Statistical time series modeling based on autoregressive, differencing, and moving-average components.
- **Exponential Smoothing:** Forecasting based on level, trend, and potentially seasonality.
- **Prophet:** Time series forecasting with trend and seasonal components.
- **Seasonal Decomposition:** Separating observed demand into trend, seasonal, and residual components.

These models are planned analytical approaches; importing the libraries does not mean that the models have already been fitted or evaluated.

## Forecast Evaluation

The notebook imports the following metrics for evaluating future forecasts:

- **Mean Absolute Error (MAE):** Measures average absolute forecast error.
- **Mean Squared Error (MSE):** Measures average squared forecast error.
- **Root Mean Squared Error (RMSE):** Measures forecast error in the original demand units.

Model comparison should use a chronological train-test split rather than a random split, preserving the temporal order of observations.

## Potential Business Applications

Once forecasting has been implemented and evaluated, the analysis could support:

1. **Demand planning:** Estimate future monthly demand.
2. **Inventory management:** Support stock planning based on expected demand.
3. **Procurement planning:** Help align purchasing decisions with anticipated demand.
4. **Seasonality analysis:** Identify recurring demand patterns that may affect planning.
5. **Forecast comparison:** Select a suitable model based on out-of-sample performance.

These are potential applications, not conclusions established by the current notebook.

## Current Project Status

The supplied notebook currently includes:

- Data loading and column renaming.
- Conversion of year and month into a datetime index.
- Chronological sorting and monthly frequency assignment.
- Visualization of historical monthly demand.

The supplied code does not yet demonstrate seasonal decomposition, model fitting, forecast generation, or evaluation results.

## Limitations and Considerations

- Missing months should be checked after assigning monthly frequency.
- Missing demand values should be investigated before modeling.
- The dataset's demand units and business context are not specified in the supplied code.
- Forecast accuracy cannot be assessed until the models are trained and tested.
- Historical patterns may not continue into future periods.
- Model performance should be compared using a consistent chronological holdout period.

## Repository Structure

```text
red-wine-demand-forecasting/
├── red_wine_demand_forecasting.ipynb
├── README.md
└── data/
    └── README.md
```

The dataset may be stored locally or documented in `data/README.md` if it cannot be redistributed.

## How to Run

1. Clone or download this repository.
2. Open `red_wine_demand_forecasting.ipynb` in Google Colab or Jupyter Notebook.
3. Upload `Red_Wine.csv`.
4. Update the dataset path if necessary.
5. Install the required libraries if they are not available.
6. Run the notebook cells in order.
7. Review the historical demand visualization and subsequent forecasting results as the project develops.

## Author

**Risty Anugrah Dwi Septiana**

- GitHub: [Ristyanugrah](https://github.com/Ristyanugrah)
- Data Analytics Portfolio: [data-analytics-portfolio](https://github.com/Ristyanugrah/data-analytics-portfolio)
- Portfolio Website: [risty-portfolio.vercel.app](https://risty-portfolio.vercel.app/)

---

*This project explores time series analysis and demand forecasting using historical monthly red wine demand data.*
