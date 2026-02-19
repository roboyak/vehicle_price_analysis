# What Drives the Price of a Car?

## Overview

This project analyzes a dataset of 426,880 used car listings from Kaggle to identify the key factors that influence used car pricing. The analysis follows the **CRISP-DM** (Cross-Industry Standard Process for Data Mining) framework and provides actionable recommendations for a used car dealership looking to optimize their inventory.

## Jupyter Notebook

The full analysis is available in the notebook: [prompt_II.ipynb](prompt_II.ipynb)

## Summary of Findings

### Top Factors Driving Used Car Prices

1. **Vehicle Age** — The single most important factor. Newer vehicles command significantly higher prices, with each additional year of age reducing value substantially.

2. **Mileage (Odometer)** — Strong negative correlation with price. Low-mileage vehicles consistently sell at a premium.

3. **Vehicle Type** — Trucks and pickups command the highest prices, followed by SUVs. Sedans and hatchbacks sit at the lower end of the price spectrum.

4. **Fuel Type** — Diesel vehicles (often trucks) tend to command higher prices. Electric and hybrid vehicles are increasingly valued.

5. **Manufacturer/Brand** — Premium and reliability-focused brands (e.g., Toyota) hold their value better in the used market.

6. **Condition** — Vehicles rated "excellent" or "like new" sell for significantly more than those in "fair" or "good" condition.

7. **Drive Type** — 4WD/AWD vehicles command a premium, particularly for trucks and SUVs.

8. **Title Status** — Clean-title vehicles far outperform salvage or rebuilt titles in resale value.

### Recommendations for Used Car Dealers

- Prioritize acquiring **newer, low-mileage vehicles** (under 5 years old)
- Stock more **trucks, SUVs, and 4WD vehicles** — these have the highest demand and pricing premiums
- Invest in **reconditioning** vehicles to "excellent" condition for better margins
- **Avoid salvage-title vehicles** unless acquisition price reflects the steep consumer discount
- Monitor the growing **EV/hybrid market** for emerging opportunities

### Methodology

- **Models Used:** Linear Regression, Ridge Regression (L2), Lasso Regression (L1)
- **Validation:** 5-fold cross-validation with GridSearchCV for hyperparameter tuning
- **Evaluation Metrics:** Mean Squared Error (MSE) and R-squared (R²)
- **Data Cleaning:** Filtered outliers, handled missing values, engineered vehicle age feature

## Repository Structure

```
vehicle_price/
├── README.md              # This file
├── prompt_II.ipynb        # Main analysis notebook
├── data/
│   └── vehicles.csv       # Used car dataset (426K listings)
└── images/
    ├── crisp.png          # CRISP-DM framework diagram
    └── kurt.jpeg          # Header image
```
