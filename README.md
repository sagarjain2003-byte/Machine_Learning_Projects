# Non-Linear Energy Demand Predictor

A machine learning project that predicts hourly household electricity demand using real-world electricity consumption data. It compares linear and nonlinear regression models and visualizes actual versus predicted power consumption.

## Project Overview

Electricity consumption changes throughout the day due to usage patterns, time, and other factors. This project analyzes historical power consumption and trains machine learning models to estimate hourly electricity demand.

The project uses the UCI Individual Household Electric Power Consumption dataset.

## Features

- Real-world electricity consumption data
- Data cleaning and missing-value handling
- Minute-level to hourly data aggregation
- Exploratory Data Analysis (EDA)
- Time-based feature engineering
- Lag features and rolling averages
- Linear Regression
- Polynomial Regression
- Random Forest Regressor
- Gradient Boosting Regressor
- Model evaluation using MAE, RMSE, and R²
- Actual vs predicted visualizations
- Feature importance analysis
- Model saving with Joblib
- Next-hour demand forecasting

## Dataset

**Source:** UCI Machine Learning Repository

Dataset: Individual Household Electric Power Consumption

https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption

The dataset contains household electricity measurements collected at approximately one-minute intervals over several years.

Target variable: `Global_active_power`

Unit: kilowatts (kW)

The project aggregates these measurements into hourly average power values.

## Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Scikit-learn
- Joblib
- Jupyter Notebook

## Machine Learning Models

| Model | Purpose |
|---|---|
| Linear Regression | Baseline prediction |
| Polynomial Regression | Learns nonlinear relationships through polynomial features |
| Random Forest Regressor | Learns nonlinear patterns and feature interactions |
| Gradient Boosting Regressor | Sequentially improves predictions using boosting |

Models are compared using the same chronological test set.

## Project Structure

```text
non-linear-energy-demand-predictor/
├── data/
│   └── household_power_consumption.txt
├── energy_demand.ipynb
├── energy_demand_model.pkl
├── model_features.pkl
├── model_comparison.csv
├── processed_energy_data.csv
├── requirements.txt
└── README.md
```

The dataset and generated model files do not have to be committed to GitHub. See the .gitignore recommendations below.

## Installation

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/non-linear-energy-demand-predictor.git
cd non-linear-energy-demand-predictor
```

### 2. Create a virtual environment (optional)

Windows:

```bash
python -m venv venv
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Download the dataset

Download the dataset from:

https://archive.ics.uci.edu/dataset/235/individual+household+electric+power+consumption

Extract the data file and place it inside the data/ folder. Ensure the notebook's file path matches your folder structure.

### 5. Run the notebook

```bash
jupyter notebook
```

Open `energy_demand.ipynb` and execute the cells in order.

## Feature Engineering

The project creates features such as:

- Hour of day
- Day of week
- Month
- Weekend indicator
- Previous-hour demand
- Previous-day demand
- Previous-week demand
- Rolling 24-hour average
- Rolling 168-hour average

These features help the models learn daily, weekly, and nonlinear consumption patterns.

## Model Evaluation

The models are evaluated using:

- **MAE:** Mean Absolute Error
- **RMSE:** Root Mean Squared Error
- **R²:** Coefficient of Determination

Actual evaluation results are generated when the notebook is executed. No fixed accuracy or performance value is claimed in advance.

## Results and Visualizations

The notebook generates:

- Electricity consumption over time
- Average demand by hour
- Demand distribution
- Actual versus predicted power consumption
- Model performance comparison
- Random Forest feature importance

Add screenshots of your actual graphs here after running the project.

## Prediction

The trained model can estimate the next hour's average household power consumption using historical demand and calendar features.

This is a household-level forecasting project, not a city-wide or national electricity demand forecasting system.

## Limitations

- The dataset represents an individual household.
- Future weather information is not included in the current model.
- Performance depends on data quality and the chronological test period.
- Next-hour forecasting requires sufficient historical hourly observations.
- Historical test performance does not guarantee future accuracy.

## Future Improvements

- Build an interactive Streamlit dashboard.
- Add weather and temperature features.
- Test XGBoost and other forecasting models.
- Experiment with LSTM neural networks.
- Add prediction intervals and stronger time-series validation.
- Deploy a forecasting interface.

## Author

**YOUR NAME**

AI/ML Student | Machine Learning | Data Science

GitHub: https://github.com/YOUR_USERNAME

LinkedIn: YOUR_LINKEDIN_URL

## License

This project is intended for educational and portfolio purposes. Check the dataset's original terms and attribution requirements before redistributing the data.

## Acknowledgements

Thanks to the UCI Machine Learning Repository for providing the household electricity consumption dataset.
