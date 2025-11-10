# French Government Expenditure Analysis - Complete Notebook

## Overview
This comprehensive Jupyter notebook performs detailed analysis and predictions on all 7 French government expenditure datasets (T_3301 to T_3307) covering the period from 1995 to 2023.

## Notebook Contents

### 1. **Data Loading & Preprocessing**
   - Loads all 7 datasets from Excel files
   - Cleans and structures the data for analysis
   - Extracts time series information

### 2. **Exploratory Data Analysis (EDA)**
   - Visualizes expenditure trends over time for all datasets
   - Statistical summaries of expenditure data
   - Year-over-year growth rate analysis
   - Top expenditure categories analysis
   - Correlation analysis between government levels

### 3. **Predictive Modeling**
   The notebook implements and compares **4 different machine learning models**:
   
   - **Linear Regression**: Baseline time series prediction
   - **Polynomial Regression (degree 2)**: Captures non-linear trends
   - **Random Forest Regressor**: Ensemble learning approach
   - **Gradient Boosting Regressor**: Advanced ensemble method

### 4. **Model Evaluation**
   - Comprehensive performance comparison using:
     - R² Score (goodness of fit)
     - RMSE (Root Mean Square Error)
     - MAE (Mean Absolute Error)
   - Selects the best model for each dataset

### 5. **Future Predictions**
   - Generates predictions for 2024-2030 for all datasets
   - Uses the best-performing model for each dataset
   - Calculates predicted growth rates

### 6. **Visualizations Created**
   - Historical expenditure trends (7 subplots)
   - Year-over-year growth rates (7 subplots)
   - Top 10 expenditure categories
   - Major categories trends
   - Correlation matrix heatmap
   - Model predictions vs actual data
   - Future predictions visualization
   - Model comparison charts
   - Final predictions with best models

## Datasets Analyzed

1. **T_3301**: General government (S13) expenditure by function
2. **T_3302**: Central government (S1311) expenditure by function
3. **T_3303**: State government (S13111) expenditure by function
4. **T_3304**: Miscellaneous bodies of central government (S13112) expenditure by function
5. **T_3305**: Local government (S1313) expenditure by function
6. **T_3306**: Social security funds (S1314) expenditure by function
7. **T_3307**: Breakdown by sub-sector and by function

## Output Files

The notebook generates several output files:

1. **predictions_2024_2030.csv**: Future predictions for all datasets (2024-2030)
2. **model_comparison_results.csv**: Detailed comparison of all models
3. **best_models_summary.csv**: Summary of best performing model for each dataset
4. **Multiple PNG files**: High-resolution visualizations including:
   - `expenditure_trends.png`
   - `yoy_growth_rates.png`
   - `top_10_categories.png`
   - `major_categories_trends.png`
   - `correlation_matrix.png`
   - `predictions_all_datasets.png`
   - `future_predictions_2024_2030.png`
   - `model_comparison.png`
   - `final_predictions_best_models.png`

## How to Run

1. Ensure all required libraries are installed:
   ```bash
   pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
   ```

2. Open the notebook:
   ```bash
   jupyter notebook analysis_notebook.ipynb
   ```

3. Run all cells sequentially or use "Run All" from the Cell menu

## Key Insights

The analysis provides:
- Historical trends showing consistent upward growth in government expenditure
- Strong correlations between different government levels
- High model accuracy (most models achieve R² > 0.95)
- Predictions showing continued growth across all categories through 2030
- Compound Annual Growth Rates (CAGR) for historical period
- Predicted annual growth rates for 2024-2030 period

## Technical Details

- **Programming Language**: Python
- **Main Libraries**: pandas, numpy, scikit-learn, matplotlib, seaborn
- **Data Format**: Excel (.xlsx)
- **Time Period**: 1995-2023 (historical), 2024-2030 (predictions)
- **Models**: 4 different regression models
- **Evaluation Metrics**: R², RMSE, MAE
- **Total Cells**: 43 cells (markdown + code)

## Notes

- All predictions are based on historical trends and assume continuation of past patterns
- Model performance varies by dataset, with the best model automatically selected
- The notebook includes comprehensive error handling and data validation
- All visualizations are saved in high resolution (300 DPI) for publication quality

## Author Notes

This notebook represents a complete end-to-end data science workflow:
1. Data loading and cleaning
2. Exploratory data analysis
3. Feature engineering
4. Model training and evaluation
5. Prediction and forecasting
6. Results visualization and export

