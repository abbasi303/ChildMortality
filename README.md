# ChildMortality

This repository analyzes, cleans, and models global child mortality data, with a focus on quality assurance, exploratory analysis, and predictive modeling. It leverages multiple open datasets to reveal trends, outliers, correlations, and country-by-country differences in child mortality, malnutrition, and regional factors.

## Project Overview

The project consists of:
- **Data loading and cleaning:** Integrates multiple sources, checks for missing values, and applies imputation and cleaning strategies.
- **Quality assurance (QA):** Performs checks to ensure data reliability and integrity throughout the workflow.
- **Exploratory Data Analysis (EDA):** Visualizes and summarizes trends in child mortality and malnutrition rates across countries, years, and genders.
- **Statistical and Predictive Analysis:** Applies correlation analysis, regression models, and clustering algorithms to uncover relationships and forecast trends.
- **Reporting:** Generates summary statistics and QA reports for documentation and transparency.

## Data Sources

- **Child_Mortality_Rate.csv:** Country-level annual data for child mortality (ages 1-4), total population, and mortality rate by gender and year.
- **World_Malnutrition_Data.csv:** Under-five mortality rates by country, gender, and year, with units as deaths per 1000 live births.
- **Region_Data.csv:** Regional malnutrition indicators (e.g., stunting rates) by area and year.

_Cleaned versions of these datasets are generated and saved in the `cleaned_data/` directory._

## Main Notebook

- **QA.ipynb:**  
  The central notebook for the entire workflow, organized into:
  1. **Data Loading:** Reads and summarizes data, inspects missing values.
  2. **Data Cleaning:** Handles missing data via interpolation and imputation; drops unnecessary columns.
  3. **EDA:** Visualizes year-by-year and country-by-country mortality trends, highlights top countries, and explores gender differences.
  4. **Statistical Analysis:** Examines correlations between mortality, population, and malnutrition. Detects outliers.
  5. **Predictive Analysis:**  
     - Linear Regression to model trends over time  
     - Polynomial Regression for complex patterns  
     - K-Means clustering to group countries with similar mortality/population profiles
  6. **Reporting:** Generates and prints QA reports for each dataset.

## How to Use

1. **Clone the repository and install requirements** (Python 3, pandas, numpy, seaborn, matplotlib, scikit-learn, scipy).
2. **Download or update data files** in the project root as needed.
3. **Open and run `QA.ipynb`** in Jupyter Notebook or JupyterLab to reproduce the analysis and generate cleaned data.

## File Structure

```
|-- QA.ipynb                      # Main Jupyter notebook
|-- Child_Mortality_Rate.csv      # Raw child mortality dataset
|-- World_Malnutrition_Data.csv   # Raw malnutrition/under-five mortality dataset
|-- Region_Data.csv               # Raw regional malnutrition/stunting dataset
|-- cleaned_data/
|    |-- cleaned_child_mortality_data.csv
|    |-- cleaned_malnutrition_data.csv
|    |-- cleaned_region_data.csv
```

## Key Features

- **Automated QA checks** at every stage of the pipeline
- **Visualization** of trends by year, country, and gender
- **Outlier detection** for high-mortality countries/years
- **Predictive modeling** for future mortality trends
- **Clustering** for comparative analysis across countries

## License

This project is for academic and research purposes. Data sources may have their own licenses—please consult the original providers.

---

For any questions or contributions, please open an issue or pull request!
