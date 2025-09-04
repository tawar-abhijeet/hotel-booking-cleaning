# hotel-booking-cleaning
This project focuses on cleaning and preprocessing the Hotel Booking Demand dataset. The goal is to transform the raw dataset into a structured, consistent, and analysis-ready format, making it easier for further exploratory data analysis (EDA), visualization, and predictive modeling.

# Hotel Bookings Data Cleaning Project <br>

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT) <br>

This repository contains a data cleaning project for a hotel bookings dataset. The primary goal was to take a raw, messy dataset and transform it into a clean, reliable, and analysis-ready format using Python and the pandas library. <br>

The entire process is documented in the `Hotel-bookings-cleaning.ipynb` Jupyter Notebook. <br>

##  Project Overview <br>
The project involved a comprehensive data cleaning process on a large dataset containing booking information for a city hotel and a resort hotel. The raw dataset contained numerous issues that would lead to inaccurate analysis, such as missing values, duplicates, and illogical data entries. <br>
This project showcases the ability to systematically identify and resolve data quality issues, preparing the data for exploratory data analysis, visualization, and machine learning tasks. <br>

##  Data Quality Issues Identified <br>
The initial analysis revealed several key problems with the raw data: <br>

1. **Missing Values**: Significant missing data in the `company`, `agent`, `country`, and `children` columns. <br>
2. **Duplicate Records**: Over 32,000 complete duplicate rows were identified. <br>
3. **Incorrect Data Types**: Columns like `children` and `agent` were incorrectly stored as floats, and date columns were stored as strings. <br>
4. **Structural Issues**: The arrival date was split across three separate columns (`arrival_date_year`, `arrival_date_month`, `arrival_date_day_of_month`). <br>
5. **Invalid & Illogical Data**: <br>
   - Bookings existed with zero total guests. <br>
   - The `adr` (Average Daily Rate) column contained negative values, which are impossible. <br>

## 🛠Cleaning Process <br>
The cleaning process was performed in a structured manner within the Jupyter Notebook: <br>

1. **Data Loading & Initial Inspection** – Loaded the data and performed a thorough initial analysis using statistical summaries (`.describe()`) and visualizations (`seaborn`, `matplotlib`). <br>
2. **Standardized Column Names** – Converted all column names to snake_case for easier access. <br>
3. **Handled Missing Values** – Applied strategies to fill or drop missing values based on the column context. <br>
4. **Combined Date Columns** – Created a single, unified `arrival_date` column from the three separate date components. <br>
5. **Corrected Data Types** – Converted columns to their appropriate data types (`float` → `int`, `object` → `datetime`). <br>
6. **Removed Duplicates & Invalid Rows** – Dropped duplicate entries and filtered out illogical rows (zero guests, negative ADR). <br>
7. **Feature Engineering** – Created useful features like `total_guests` and `total_nights`. <br>
8. **Final Export** – Exported the fully cleaned dataset to `hotel_bookings_cleaned.csv`. <br>

## Tools and Libraries Used <br>
- **Python** <br>
- **Pandas** – Data manipulation and cleaning <br>
- **Matplotlib & Seaborn** – Data visualization <br>
- **Jupyter Notebook** – Project environment <br>

## Results <br>
The cleaning process had a significant impact on the dataset’s quality and reliability: <br>

- **Total Rows Removed**: **32,608 rows** (27.31% of the dataset) were removed due to duplicates and invalid data. <br>
- **Final Dataset**: Clean, consistent, and ready for accurate analysis with no critical missing values or duplicates. <br>

## 📜 License <br>
This project is licensed under the MIT License. <br>
