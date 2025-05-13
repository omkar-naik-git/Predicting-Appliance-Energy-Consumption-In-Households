# Predicting Appliance Energy Consumption in Households

This project aims to develop a machine learning model to predict household appliance energy consumption using a range of environmental and time-based features. By leveraging advanced data preprocessing, feature engineering, and modeling techniques, the project helps in optimizing energy usage, reducing costs, and improving overall efficiency.

##  Objective

To predict energy consumption (in Wh) of appliances using a supervised regression model trained on environmental and time-related data.

##  Importance

* Enables energy optimization in households.
* Supports cost-saving and energy efficiency.
* Provides insights for smart home systems.

##  Dataset

* **Name:** `energydata_complete.csv`
* **Rows:** 19,735
* **Features:** 29
* **Target Variable:** `Appliances` (energy consumption in Wh)
* **Key Features:** Temperature, Humidity, Date-Time, Weather Conditions

##  Workflow Overview

1. **Data Preprocessing**

   * Convert date column to datetime format
   * Extract hour, day, month, weekday, and weekend indicators
   * Standardize numerical features using `StandardScaler`
   * Create engineered features (e.g., temperature-humidity ratio, sinusoidal time encodings)

2. **Exploratory Data Analysis (EDA)**

   * Histograms and summary statistics
   * Correlation heatmaps
   * Identification of key variables

3. **Feature Engineering**

   * Selection based on absolute correlation > 0.05
   * Engineered features: outdoor temp variation, hour of day (sin/cos), pressure-humidity interaction

4. **Model Development & Evaluation**

   * Models used:

     * Linear Regression (Baseline)
     * Random Forest Regressor
     * Gradient Boosting Regressor
     * XGBoost Regressor
     * Voting Regressor (Ensemble)
     * Deep Neural Network
   * Evaluation Metrics: R² Score, MAE, MSE
   * **Best Model:** Random Forest Regressor (R² = 0.5598)

5. **Hyperparameter Tuning**

   * GridSearchCV for tree-based models
   * Neural Network with dropout, Adam optimizer, and 3 hidden layers

##  Feature Importance

Top features influencing energy usage:

* Outdoor Temperature Variation
* Temperature-Humidity Ratio
* Encoded Hour of the Day

##  Future Work

* Implement stacking and blending ensemble methods
* Explore LSTM networks for capturing time-series patterns
* Integrate real-time prediction systems for smart home devices

