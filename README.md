# French Government Expenditure Analysis

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Python 3.14+](https://img.shields.io/badge/python-3.14+-blue.svg)](https://www.python.org/downloads/)

A comprehensive data analysis and machine learning project that analyzes French government expenditure data from 1995-2023 and generates predictions through 2030 using multiple regression models.

## 📊 Overview

This project performs in-depth analysis of French government expenditure across different administrative levels and functions. It uses historical data to identify trends, patterns, and correlations, then applies machine learning algorithms to forecast future expenditure through 2030.

The analysis covers seven distinct datasets representing different government sectors:
- General government expenditure
- Central government expenditure
- State government expenditure
- Miscellaneous central government bodies
- Local government expenditure
- Social security funds
- Breakdown by sub-sector and function

## ✨ Features

- **Comprehensive Data Analysis**: Processes 7 government expenditure datasets (T_3301 to T_3307)
- **Time Series Analysis**: Analyzes trends from 1995 to 2023 (29 years of data)
- **Multiple ML Models**: Implements and compares 4 different regression models:
  - Linear Regression
  - Polynomial Regression (degree 2)
  - Random Forest Regressor
  - Gradient Boosting Regressor
- **Future Predictions**: Generates forecasts for 2024-2030
- **Rich Visualizations**: Creates 9+ high-quality charts and graphs
- **Model Performance Metrics**: Evaluates models using R², RMSE, and MAE
- **Automated Model Selection**: Automatically selects the best model for each dataset
- **Export Capabilities**: Saves predictions and results to CSV files

## 📁 Project Structure

```
French_Government_Expenditure_Analysis/
├── datasets/                          # Raw data files
│   ├── T_3301.xlsx                   # General government (S13)
│   ├── T_3302.xlsx                   # Central government (S1311)
│   ├── T_3303.xlsx                   # State government (S13111)
│   ├── T_3304.xlsx                   # Misc. central government (S13112)
│   ├── T_3305.xlsx                   # Local government (S1313)
│   ├── T_3306.xlsx                   # Social security funds (S1314)
│   └── T_3307.xlsx                   # Breakdown by sub-sector
├── analysis_notebook.ipynb            # Main analysis notebook
├── analysis_notebook_executed.ipynb   # Executed version with outputs
├── main.py                           # Python entry point
├── pyproject.toml                    # Project dependencies
├── ANALYSIS_README.md                # Detailed analysis documentation
├── predictions_2024_2030.csv         # Future predictions
├── model_comparison_results.csv      # Model performance comparison
├── best_models_summary.csv           # Best model for each dataset
├── *.png                             # Generated visualizations
├── French_Government_Expenditure_Analysis.pptx  # Presentation
├── LICENSE                           # MIT License
└── README.md                         # This file
```

## 🚀 Getting Started

### Prerequisites

- Python 3.14 or higher
- pip package manager

### Installation

1. Clone the repository:
```bash
git clone <repository-url>
cd French_Government_Expenditure_Analysis
```

2. Install dependencies:
```bash
pip install pandas numpy matplotlib seaborn scikit-learn openpyxl jupyter
```

Or if using UV package manager:
```bash
uv sync
```

### Usage

#### Option 1: Run Jupyter Notebook (Recommended)

```bash
jupyter notebook analysis_notebook.ipynb
```

Then run all cells sequentially or use "Cell > Run All" from the menu.

#### Option 2: Run Python Script

```bash
python main.py
```

## 📈 Analysis Components

### 1. Data Loading & Preprocessing
- Loads all 7 Excel datasets
- Cleans and structures data
- Extracts time series information

### 2. Exploratory Data Analysis (EDA)
- **Expenditure Trends**: Visualizes historical spending patterns
- **Growth Rate Analysis**: Calculates year-over-year changes
- **Top Categories**: Identifies highest spending areas
- **Correlation Analysis**: Examines relationships between government levels
- **Statistical Summaries**: Provides descriptive statistics

### 3. Machine Learning Models

The project implements four regression models:

| Model | Description | Use Case |
|-------|-------------|----------|
| Linear Regression | Baseline model | Simple linear trends |
| Polynomial Regression | Degree 2 polynomial | Non-linear patterns |
| Random Forest | Ensemble method | Complex relationships |
| Gradient Boosting | Advanced ensemble | Best overall accuracy |

### 4. Model Evaluation

Models are evaluated using:
- **R² Score**: Goodness of fit (higher is better)
- **RMSE**: Root Mean Square Error (lower is better)
- **MAE**: Mean Absolute Error (lower is better)

Most models achieve **R² > 0.95**, indicating excellent fit.

### 5. Future Predictions

- Generates predictions for 2024-2030 (7 years)
- Uses the best-performing model for each dataset
- Calculates predicted growth rates
- Exports results to CSV files

## 📊 Generated Outputs

### CSV Files
- `predictions_2024_2030.csv` - Future expenditure predictions
- `model_comparison_results.csv` - Detailed model performance metrics
- `best_models_summary.csv` - Best model selection summary

### Visualizations (PNG files)
1. `expenditure_trends.png` - Historical trends across all datasets
2. `yoy_growth_rates.png` - Year-over-year growth analysis
3. `top_10_categories.png` - Highest expenditure categories
4. `major_categories_trends.png` - Major category trends over time
5. `correlation_matrix.png` - Correlation heatmap between sectors
6. `predictions_all_datasets.png` - Model predictions vs actual data
7. `future_predictions_2024_2030.png` - Future forecasts
8. `model_comparison.png` - Model performance comparison
9. `final_predictions_best_models.png` - Best model predictions

### Presentation
- `French_Government_Expenditure_Analysis.pptx` - Summary presentation

## 🔍 Key Insights

- **Consistent Growth**: Government expenditure shows steady upward trend from 1995-2023
- **Strong Correlations**: High correlation between different government levels
- **High Accuracy**: Most models achieve R² scores above 0.95
- **Continued Growth**: Predictions indicate continued expenditure increase through 2030
- **Social Security**: Represents significant portion of government spending
- **Local Government**: Shows unique spending patterns compared to central government

## 🛠️ Technologies Used

- **Python 3.14+**: Core programming language
- **pandas**: Data manipulation and analysis
- **NumPy**: Numerical computing
- **scikit-learn**: Machine learning algorithms
- **Matplotlib**: Data visualization
- **Seaborn**: Statistical visualizations
- **Jupyter**: Interactive notebook environment
- **openpyxl**: Excel file handling
- **python-pptx**: PowerPoint generation

## 📚 Datasets

The project analyzes French government expenditure data from INSEE (Institut national de la statistique et des études économiques):

| Dataset | Description | Government Level |
|---------|-------------|------------------|
| T_3301 | General government | S13 |
| T_3302 | Central government | S1311 |
| T_3303 | State government | S13111 |
| T_3304 | Miscellaneous central government | S13112 |
| T_3305 | Local government | S1313 |
| T_3306 | Social security funds | S1314 |
| T_3307 | Sub-sector breakdown | All |

**Time Period**: 1995-2023 (historical), 2024-2030 (predictions)

## ⚠️ Limitations & Assumptions

- Predictions assume continuation of historical trends
- External factors (economic crises, policy changes) not explicitly modeled
- Model performance varies by dataset
- Predictions become less reliable further into the future

## 📄 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 👤 Author

**PAUL MICKY D COSTA**

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

## 📝 Notes

This project demonstrates a complete end-to-end data science workflow:
1. Data collection and loading
2. Data cleaning and preprocessing
3. Exploratory data analysis
4. Feature engineering
5. Model training and evaluation
6. Prediction and forecasting
7. Results visualization and export

All visualizations are generated in high resolution (300 DPI) for publication quality.

## 📞 Support

For questions or issues, please open an issue in the repository.

---

**Made with ❤️ and Python**

