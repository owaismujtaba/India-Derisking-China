# Inda-Derisking-Visa-Viz-China

## Table of Contents
1.  Introduction
2.  Project Structure
3.  Data Source
4.  Notebooks
    *   `Import_Export_Data_Cleaning.ipynb`
    *   `Import_Export_Analysis.ipynb`
    *   `Chinese_Dependence.ipynb`
    *   `Commodity_Analysis.ipynb`
5.  Results and Visualizations (Example)
6.  Conclusion and Future Work

## 1. Introduction

This project aims to analyze India's trade data, with a specific focus on understanding and visualizing its trade relationships, particularly concerning imports and exports with China. The goal is to identify patterns, dependencies, and potential areas for "derisking" India's trade reliance on specific countries or commodities. This analysis will involve cleaning raw trade data, performing time-series analysis, and examining commodity-level import trends.

## 2. Project Structure

The project is organized into several directories to manage raw data, processed data, and notebooks effectively.

```
.
├── data/
│   ├── exports/
│   │   └── country_wise/
│   ├── imports/
│   │   ├── commodity_wise_china/
│   │   ├── country_wise/
│   │   └── CommodityWiseAll/
│   ├── Import_Export_Data_Cleaning.ipynb
│   ├── Import_Export_Analysis.ipynb
│   ├── Chinese_Dependence.ipynb
│   ├── Commodity_Analysis.ipynb
├── cleaned_data/
│   ├── CountryWiseImports.csv
│   ├── CommodityWiseImports.csv
│   └── ... (other processed data files)
├── README.md
```


## 3. Data Source

The raw data is expected to be in `.xlsx` format, downloaded ***from https://tradestat.commerce.gov.in/***

### 3.1. For Exports Data
1.  Download the Exports data Select Country-wise(Reports) and Country(All) for years 2018-2025 and put in the **Directory: `data/exports/country_wise`**

### 3.2. For Imports Data
1.  Download the Imports data Select Country-wise(Reports) and Country(All) for years 2018-2025 and put in the **Directory: `data/imports/country_wise`**
2.  Download the Imports data Country-Wise all Commodities(Reports) and Country(CHINA P RP) for years 2018-2025 and put in the **Directory: `data/imports/commodity_wise_china`**
3.  Download the Imports data Commodity x Country-wise(Reports) and Country(CHINA P RP) for years 2018-2025 and put in the **Directory: `data/imports/CommmodityWiseAll`**
    For each commodity, create a folder with the name as `HSCode_X` (e.g., `HSCode_85`) and put the respective data there.

## 4. Notebooks

This project includes several Jupyter notebooks, each designed for a specific part of the data processing and analysis pipeline.

### 4.1. `Import_Export_Data_Cleaning.ipynb`
This notebook is dedicated to the initial data preparation steps:
1.  **Locate and read** multiple Excel files for different trade categories (imports by country, exports by country, imports by commodity).
2.  **Standardize headers** and extract relevant columns to ensure data consistency.
3.  **Consolidate data** from various years and files into a single, clean DataFrame, ready for analysis.
4.  **Save the cleaned data** into easily accessible CSV files in the `processed_data/` directory for further analysis or visualization.

### 4.2. `Import_Export_Analysis.ipynb`
This notebook focuses on high-level analysis of India's overall trade:
1.  **Time-series plots for imports and exports**: Visualize the trends of India's total imports and exports over time.
2.  **Export-Import Ratio**: Calculate and plot the ratio of exports to imports to understand India's trade balance.

### 4.3. `Chinese_Dependence.ipynb`
This notebook dives deeper into India's trade relationship with China:
1.  **Imports Country-level contribution charts**: Generate visualizations showing the contribution of various countries to India's total imports, highlighting China's share.
2.  **Dominance Index of China**: Develop and visualize a dominance index to quantify India's reliance on China for imports.
3.  **Import share of top 5 countries**: Compare China's import share against other top importing countries.

### 4.4. `Commodity_Analysis.ipynb`
This notebook provides a detailed look at commodity-level trade with China:
1.  **Top 5 Contributing commodities (Imports) (CHINA)**: Identify and visualize the top 5 commodities imported from China.
2.  **% Share of top 5 Commodities (Imports) (CHINA)**: Analyze the percentage share of these top commodities in India's total imports from China.
3.  **Trend Plots of Import Ratio (CHINA/WORLD) Commodity level**: Plot time-series trends of the import ratio for specific commodities (China's share of world imports for that commodity) to gauge China's global dominance in those sectors and India's reliance.



