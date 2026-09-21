
# Investor Behavior Analytics - Data Cleaning & Visualization (Phase 2)

## Overview
This project performs end-to-end data processing, cleaning, and exploratory visual analysis on the investor behavior dataset using Python in Google Colab.

## Key Pipeline Steps
1. **Data Ingestion**: Loaded `investment - Copy.csv` into a Pandas DataFrame.
2. **Data Cleaning & Preprocessing**:
   - Identified and removed duplicate rows.
   - Handled missing numeric values using **median imputation**.
   - Handled missing categorical values using **mode imputation** and removed extra whitespace.
3. **Exploratory Data Analysis (EDA)**:
   - Evaluated data distributions using Seaborn histograms.
   - Analyzed category distributions via horizontal bar charts.
   - Built correlation heatmaps to assess relationships across numeric variables.

## Tools & Libraries Used
- **Environment**: Google Colab / Jupyter
- **Data Manipulation**: `pandas`, `numpy`
- **Visualization**: `matplotlib`, `seaborn`
