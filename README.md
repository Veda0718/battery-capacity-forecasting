# Lithium-Polymer Battery Capacity Prediction

## Overview

This project builds a machine learning model to predict Lithium-Polymer (LiPo) battery capacity degradation across repeated charge–discharge cycles. Using a publicly available Kaggle dataset containing experimental measurements from five LiPo batteries under Standard and Stress load conditions, the analysis converts high-frequency voltage and charge readings into cycle-level features that capture electrochemical aging behavior.

LiPo batteries are widely used in electric vehicles, renewable energy storage, drones, and consumer electronics but naturally lose capacity and voltage stability over time. Predicting this degradation is essential for improving battery lifespan, safety, manufacturing optimization, sustainability, and predictive maintenance planning.

By modeling capacity decline and identifying the most influential performance indicators, this project demonstrates how data-driven insights can support operational decision-making and lifecycle forecasting for lithium-based energy systems.

## Tools
Python, Pandas, NumPy, Scikit-Learn, XGBoost, Matplotlib, Seaborn, SHAP

## Project Workflow
 - Loaded and explored three raw datasets containing capacity, voltage, and charge measurements.
 - Aggregated high-frequency sensor data into cycle-level features and merged datasets on (battery_id, cycle_number).
 - Handled missing values using linear interpolation to maintain degradation trends.
 - Engineered delta-based features comparing Standard vs Stress conditions.
 - Trained and evaluated regression models (Linear Regression, Random Forest, XGBoost) to predict capacity_Ah.
 - Interpreted results using feature importance and SHAP to explain degradation drivers.

Results
| Model | R² | RMSE |
|---|---|---|
| Linear Regression | 0.85 | 0.039 |
| Random Forest (Best) | 0.95 | 0.023 |
| XGBoost | 0.91 | 0.030 |

**Key Insight:** voltage_delta_mean and cycle_number are the strongest predictors, enabling early detection of battery health decline and supporting predictive maintenance strategies.

For full methodology, plots, SHAP visuals, and business insights, see Final Report.pdf
