# House Price Data Cleaning

This repository contains a Jupyter Notebook (`House_Price Data Cleaning.ipynb`) that performs data cleaning on a housing dataset (`housing2.csv`). Below is a summary of the work done in the notebook.

## Overview

The notebook focuses on loading and preparing a housing dataset for analysis. The dataset contains information about house prices and related features such as location, housing age, number of rooms, population, and income levels.

## Steps Performed

1. **Import Libraries**  
   - The notebook imports essential Python libraries for data manipulation and visualization:
     - `pandas` for data handling and analysis
     - `numpy` for numerical operations
     - `matplotlib.pyplot` and `seaborn` for data visualization
     - `missingno` for visualizing missing data

2. **Connect to Google Drive**  
   - The notebook mounts Google Drive to access the dataset stored at `/content/drive/MyDrive/DataSets/housing2.csv`.

3. **Read Data**  
   - The dataset is loaded into a pandas DataFrame using `pd.read_csv()`.
   - The dataset contains 20,640 rows and 9 columns:
     - `longitude`: Longitude of the house location
     - `latitude`: Latitude of the house location
     - `housing_median_age`: Median age of houses
     - `total_rooms`: Total number of rooms
     - `total_bedrooms`: Total number of bedrooms
     - `population`: Population in the area
     - `households`: Number of households
     - `median_income`: Median income of residents
     - `median_house_value`: Median house value (target variable)

## Notes
- The dataset appears to have missing values (e.g., `NaN` in `housing_median_age` and `population` for some rows), which may require further cleaning steps such as imputation or removal.
- The notebook includes a deprecated warning related to the `interpolation` argument in NumPy's `percentile` function, suggesting a need to update to `method` for compatibility with newer NumPy versions.

## Usage
To run the notebook:
1. Ensure you have access to the dataset file (`housing2.csv`) in the specified Google Drive path.
2. Install required libraries: `pandas`, `numpy`, `matplotlib`, `seaborn`, and `missingno`.
3. Run the notebook in a Jupyter environment (e.g., Google Colab) with Google Drive mounted.

## Future Work
- Handle missing values in the dataset (e.g., using imputation or dropping rows).
- Address the NumPy deprecation warning by updating the `percentile` function call.
- Perform additional data cleaning, such as outlier detection and handling.
- Conduct exploratory data analysis (EDA) to understand relationships between features and the target variable (`median_house_value`).