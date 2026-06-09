# Urban Bike-Sharing Demand Forecasting & Analysis

## Project Overview
This project was developed as a comprehensive data analysis and forecasting solution for the **City Smart Mobility Taskforce**. The initiative addresses two primary municipal challenges regarding public bike-sharing infrastructure:
1. **Operational Fleet Optimization:** Forecasting hourly rental demand to proactively rebalance the bike fleet across docking stations.
2. **Strategic Infrastructure Planning:** Identifying citizen usage patterns (commute vs. leisure, weather resilience) to justify future budget allocations for new bike lanes and stations.


## Objectives
* **Exploratory Data Analysis (EDA):** Uncover behavioral patterns in ridership using Python (`matplotlib`, `seaborn`) to map out how weather, holidays, and time of day impact bike usage.
* **Time Series Forecasting:** Implement time series analysis models to predict hourly bike demand for a 7-day operational window.
* **Interactive Dashboarding:** Develop a Power BI dashboard equipped with DAX measures to provide city planners with a dynamic, filterable view of the network's performance.

## Repository Structure
```text
bike_sharing_project/
├── data/
│   ├── raw/               # Original datasets (excluded via .gitignore)
│   └── processed/         # Cleaned data exported for Power BI
├── notebooks/
│   ├── 01_data_cleaning_and_eda.ipynb    # Data prep and visual storytelling
│   └── 02_time_series_forecasting.ipynb  # ARIMA/SARIMA modeling and evaluation
├── assets/                # Presentation slides and visual assets
├── requirements.txt       # Python environment dependencies
└── README.md              # Project documentation
```text

## Tech Stack & Tools
* Programming & Analysis: Python (Jupyter Notebooks in VS Code)
* Data Manipulation: pandas, numpy
* Data Visualization: matplotlib, seaborn
* Statistical Modeling: statsmodels (for Time Series Analysis)
* Business Intelligence: Microsoft Power BI (DAX, Data Modeling)

## How to Run the Project
* Clone this repository to your local machine.
* Install the required Python packages using pip install -r requirements.txt.
* Place the raw dataset (train.csv, test.csv) into the data/raw/ directory.
* Run the Jupyter notebooks sequentially to generate the processed data and view the analysis.
* Open the .pbix file (if included) in Power BI Desktop to interact with the final dashboard.