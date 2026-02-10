# Predictive Analysis - Electric Vehicle Battery Degradation

## Overview

This analysis combines **Machine Learning** with **Interactive 3D Visualizations** to understand how multiple factors simultaneously affect electric vehicle battery degradation.

## Machine Learning Models

### Algorithms Used:
1. **Random Forest Regressor**
   - 200 decision trees
   - Maximum depth: 15
   - Excellent for capturing non-linear relationships
   
2. **Gradient Boosting Regressor**
   - 200 estimators
   - Learning rate: 0.1
   - Great for precise predictions

### Evaluation Metrics:
- **R² Score**: Percentage of variance explained
- **MAE (Mean Absolute Error)**: Average absolute error in %
- **RMSE (Root Mean Squared Error)**: Penalizes large errors

## Key Expected Insights

### Factors That Accelerate Degradation:
- **Cumulative Charging Cycles**: More use = more wear
- **Extreme Temperature**: Both cold and heat degrade the battery
- **Frequent Fast Charging**: Convenient, but accelerates degradation
- **Aggressive Driving**: High discharge rates stress the battery
- **Age**: Natural degradation over time

### Protective Factors:
- **Moderate Temperature** (15-25°C): Ideal for longevity
- **Slow Charging**: Healthier for the battery
- **Smooth Driving**: Less electrical stress
- **Avoid Extremes**: Don't leave the battery too full or empty



## Technical Methodology

### Data Preparation:
1. Encoding categorical variables (Label Encoding)
2. Train/test split (80/20)
3. Feature standardization

### Training:
1. Training multiple models
2. Cross-validation
3. Selection of best model based on R²

### Prediction:
1. Creating value grid for 3D surface
2. Prediction for all grid points
3. Interpolation for smooth visualization

## Data Structure

### Input Variables (Features):
- **Battery_Capacity_kWh**: Battery capacity
- **Vehicle_Age_Months**: Vehicle age
- **Total_Charging_Cycles**: Cumulative charging cycles
- **Avg_Temperature_C**: Average operating temperature
- **Fast_Charge_Ratio**: Proportion of fast charges
- **Avg_Discharge_Rate_C**: Average discharge rate
- **Driving_Style**: Driving style (Conservative/Moderate/Aggressive)
- **Internal_Resistance_Ohm**: Internal resistance
- **SoH_Percent**: Battery State of Health (0-100%)

*Making complex battery degradation patterns visible and actionable*
