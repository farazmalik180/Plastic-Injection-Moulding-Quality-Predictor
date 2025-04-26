# Plastic-Injection-Moulding-Quality-Predictor

The client, a manufacturer in the plastic injection moulding sector, aimed to predict product quality ("Waste," "Acceptable," "Target," "Inefficient") to optimize production and reduce defects. Their goal was to develop an interactive Streamlit dashboard for real-time quality predictions using process parameters like temperature and pressure.

Challenges included:

File Mismatches: Dataset.csv naming issues caused FileNotFoundError; resolved by updating code to match the correct case (Dataset.csv) and adding upload prompts.
Feature Mismatch: A ValueError arose due to inconsistent feature counts (13 vs. 14) after adding pressure_ratio; fixed by ensuring preprocessing consistency.
LightGBM Warnings: "No further splits" warnings indicated overfitting; mitigated by tuning parameters (max_depth=5, min_data_in_leaf=20).

Deployment in Colab: Ngrok authentication and runtime resets posed issues; addressed by integrating an authtoken and robust file checks.

The solution involved preprocessing, feature engineering (pressure_ratio), training RandomForest and LightGBM models, and deploying a dashboard with single/batch prediction capabilities, static visualizations, and statistics, enabling the client to monitor and improve moulding quality effectively.
