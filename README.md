# Pharmacy Demand Forecasting & Inventory Risk Analytics

## Project Overview

This project combines **time series forecasting**, **inventory optimization**, and **machine learning-based risk prediction** to support pharmaceutical supply chain management.

The objective is to help hospital pharmacies and healthcare organizations:

- Forecast future medication demand
- Identify high-risk products for stockouts
- Prioritize inventory using ABC analysis
- Improve purchasing and replenishment decisions
- Reduce medication shortages and excess inventory

---

## Business Problem

Hospital pharmacies often face two major challenges:

1. **Stockouts**
   - Critical medications become unavailable.
   - Can delay treatment and impact patient outcomes.

2. **Overstocking**
   - Excess inventory increases holding costs.
   - Risk of drug expiration and waste.

This project develops a data-driven framework to address both issues through forecasting and predictive analytics.

---

## Dataset

The dataset contains pharmacy transaction records including:

- Transaction Date
- Drug Name
- Drug Type
- Dosage Form
- Quantity Sold
- Sales Information
- Inventory-related attributes

---

# Exploratory Data Analysis (EDA)

The analysis includes:

### Dataset Quality Assessment
- Missing Values Analysis
- Duplicate Records Detection
- Data Type Validation

### Sales Analysis
- Top Selling Drugs
- Drug Type Distribution
- Dosage Form Analysis
- Daily Sales Trend
- Monthly Sales Trend
- Day-of-Week Analysis
- Hourly Sales Analysis

### Business Insights
- Top Product Contribution Analysis
- Sales Pattern Identification
- Demand Seasonality Exploration

---

# Demand Forecasting

## Prophet Forecasting Model

Facebook Prophet is used to forecast future medication demand.

### Steps

1. Data Preparation
2. Time Series Aggregation
3. Prophet Model Training
4. Forecast Generation
5. Seasonality Analysis

### Outputs

- Future Demand Forecast
- Trend Components
- Weekly Seasonality
- Yearly Seasonality
- Forecast Confidence Intervals

### Forecast Horizon

- Next 90 Days

---

# Inventory Optimization

## ABC Inventory Analysis

ABC Analysis classifies medications based on cumulative sales contribution.

### Category A
- Highest business impact
- Tight inventory control required

### Category B
- Moderate importance

### Category C
- Lower contribution products

### Deliverables

- ABC Classification
- Product Ranking
- Inventory Distribution Visualization

---

# Demand Risk Prediction

## XGBoost Classification Model

A machine learning model is developed to identify products at risk of experiencing unusually high demand.

### Feature Engineering

Features include:

- Time Features
  - Day
  - Month
  - Weekday
  - Quarter

- Historical Demand Features

- Product Characteristics

### Target Variable

- High Demand Risk Label

---

# Machine Learning Pipeline

1. Data Cleaning
2. Feature Engineering
3. Feature Selection
4. Train-Test Split
5. XGBoost Model Training
6. Performance Evaluation
7. Model Explainability

---

# Model Evaluation

Evaluation metrics include:

- Accuracy
- Precision
- Recall
- F1 Score
- ROC-AUC

### Additional Validation

#### Calibration Analysis
Measures how well predicted probabilities reflect actual outcomes.

#### Brier Score
Evaluates probabilistic prediction quality.

#### Calibration Curve
Visual comparison between predicted and observed risk.

---

# Explainable AI (XAI)

## SHAP Analysis

SHAP (SHapley Additive exPlanations) is used to interpret model predictions.

### Visualizations

- SHAP Summary Plot
- SHAP Feature Importance Plot
- SHAP Waterfall Plot

### Benefits

- Understand key demand drivers
- Improve model transparency
- Support decision-making by pharmacy managers

---

# Decision Curve Analysis (DCA)

Decision Curve Analysis evaluates the clinical/business utility of the predictive model.

### Purpose

Determine whether the model provides more value than:

- Treat All Strategy
- Treat None Strategy

### Outcome

Supports practical deployment decisions by quantifying net benefit across multiple risk thresholds.

---

# Technologies Used

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Prophet
- Scikit-Learn
- XGBoost
- SHAP

---

# Key Business Recommendations

### Forecast-Driven Procurement
Use demand forecasts to optimize purchasing schedules.

### Inventory Prioritization
Focus inventory control efforts on Category A medications.

### Early Warning System
Deploy the XGBoost model to identify products with elevated demand risk.

### Stockout Prevention
Monitor high-risk products proactively and adjust reorder points.

### Data-Driven Pharmacy Operations
Leverage predictive analytics to improve operational efficiency and patient care continuity.

---

# Future Improvements

- Real-time forecasting dashboard
- Automated replenishment recommendations
- Safety stock optimization
- Multi-product forecasting models
- Integration with hospital ERP systems
- MLOps deployment pipeline
- Causal analysis of demand drivers

---
