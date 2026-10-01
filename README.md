# Freight Rate Prediction - Spotter Assessment

This repository contains the machine learning solution for predicting freight rates (posted_rate) using the Spotter dataset. The model addresses data quality issues, handles spatial and temporal features, and generates structured rate predictions along with visual performance analysis.

## Project Structure
- solution.ipynb: Complete data cleaning, feature engineering, model training, and evaluation pipeline.
- validation_predictions.csv: Model predictions generated for the validation dataset (12,000 rows).
- december_predictions.csv: Model predictions generated for December 2025 chart inputs (31 rows).
- scorer_results/candidate_december.png: Generated chart output visualizing predicted rates across December dates.
- score.py: Evaluation script used to validate submission formats and output results.

## Approach & Methodology

1. *Data Preprocessing & Cleaning:*
   - *Outlier Handling:* Corrected negative values in the weight column by taking their absolute values and imputing missing values with the median.
   - *Datetime Processing:* Extracted temporal features (month, day, dayofweek) from the load dates to capture seasonality and day-of-week rate fluctuations.
   - *Categorical Encoding:* Applied Label Encoding across categorical variables (equipment_type, origin/destination identifiers).

2. *Model Selection:*
   - Evaluated and trained a *RandomForestRegressor* to effectively capture non-linear relationships and feature interactions across load attributes (distance, weight, route specifics).

3. *Validation & Evaluation:*
   - Verified that output schema requirements match the target benchmark formats exactly.
   - Successfully executed score.py to produce final validation checks and output visualization charts.

## How to Run locally

1. Clone the repository:
   ```bash
   git clone [https://github.com/aboodbargash373-png/ML_freight_Assessment.git](https://github.com/aboodbargash373-png/ML_freight_Assessment.git)
   cd ML_freight_Assessment# ML_freight_Assessment
