# Smart Mobility Taskforce: Predictive Demand & Fleet Logistics

[Power BI Dashboard Link]  - https://app.powerbi.com/links/fVrIc8tQJY?ctid=b30f4b44-46c6-4070-9997-f87b38d4771c&pbi_source=linkShare&bookmarkGuid=940bb9bd-7e15-4c58-8679-545cb3a21879

## Executive Summary

### The Problem

The city's bike-sharing network relied on reactive logistics, resulting in localized vehicle shortages during daily commuter peaks and unpredictable system under-utilization during severe weather events.

### The Solution

A SARIMA time-series forecasting model was developed to predict bike demand up to 168 hours in advance. These predictive outputs were integrated into an interactive Power BI dashboard, enabling stakeholders to transition from reactive fleet management to proactive, data-driven decision-making.

## Stakeholders and Value Proposition

### Fleet Operations Manager (Logistics)

* Optimize daily truck redistribution schedules using 168-hour demand forecasts.
* Reduce uncertainty through forecast confidence intervals.
* Improve fleet availability during peak demand periods.

### Urban Planner (Strategy)

* Analyze long-term seasonal and behavioral trends.
* Understand commuter versus tourist usage patterns.
* Evaluate the impact of extreme weather on ridership to support infrastructure planning.

## Deliverables

### Interactive Power BI Dashboard

[Interactive Power BI Dashboard]([INSERT YOUR POWER BI LINK HERE])

*Note: Dashboard access may require organizational permissions. For offline viewing, the `.pbix` file is available in the `dashboard/` directory.*

### Executive Presentation Deck

Available in the `presentation/` directory.

## Technical Architecture and Methodology

### 1. Data Engineering and Exploratory Data Analysis (Python/Pandas)

* Verified chronological data integrity and enforced strict DateTime formatting.
* Extracted temporal features including hour, day type, and month from the datetime index.
* Identified distinct commuter and leisure usage patterns through temporal analysis.
* Quantified weather sensitivity, showing that Category 3 weather conditions reduced median rentals by approximately 50%, while Category 4 conditions resulted in near-total system shutdown.

### 2. Time-Series Forecasting (SARIMA)

#### Model Selection

Traditional ARIMA models were insufficient for capturing recurring daily and weekly demand patterns. SARIMA was selected to model both short-term trends and seasonal commuter cycles.

#### Validation Strategy

* Trained on historical rental data.
* Evaluated using a dedicated 168-hour holdout test set.

#### Performance

* Mean Absolute Error (MAE): **56.04 bikes**
* Forecast accuracy provided an actionable margin of error for operational planning and fleet redistribution.

### 3. Interactive Visualization (Power BI)

* Designed a stakeholder-focused dashboard with dedicated views for:

  * Strategic Planning
  * Fleet Logistics
* Implemented advanced DAX calculations using:

  * `CALCULATE()`
  * `DIVIDE()`
  * `VAR`
  * `ABS()`
* Added interactive features including:

  * Dynamic cross-filtering
  * Drill-down analysis
  * Timeline zoom slider for hour-level forecasting insights

## Repository Structure

```text
├── data/
│   ├── raw/                  # Original unprocessed dataset
│   └── processed/            # Cleaned historical data and SARIMA forecast outputs
├── notebooks/
│   └── 01_data_cleaning_and_time_series_forecasting.ipynb
├── dashboard/
│   └── Smart_Mobility_Taskforce.pbix
├── presentation/
│   └── DSAI3301_Final_Project_Presentation.pdf
└── README.md
```

## Tools and Technologies

* Python
* Pandas
* NumPy
* Matplotlib
* Statsmodels (SARIMA)
* Power BI
* DAX

## Key Outcomes

* Enabled proactive fleet redistribution through 168-hour demand forecasting.
* Improved operational readiness during peak commuting periods.
* Quantified the impact of weather conditions on bike-sharing demand.
* Delivered an interactive decision-support dashboard for logistics and strategic planning teams.
