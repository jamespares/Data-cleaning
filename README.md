# Store Income Data Cleaning and Preparation

Preparing the 'store_income_data_task.csv' dataset for analysis by cleaning inconsistencies in the 'country' column and calculating a new 'days_ago' feature. This facilitates accurate and time-sensitive insights into store income data.

**Data Overview:**

store_income_data_task.csv: Dataset containing store income data, including:
country: The store's country location.
date_measured: The date when income was recorded.

**Steps:**

Data Loading:

Import necessary libraries (pandas, NumPy, datetime).
Load the 'store_income_data_task.csv' using pd.read_csv().
Cleaning the 'country' Column:

Identify Inconsistencies: Display unique values in the 'country' column to reveal variations in capitalization, punctuation, and abbreviations.
Lowercase and Trim: Convert values to lowercase with .str.lower() and remove trailing whitespace with .str.strip().

Standardisation:
Create a mapping dictionary (country_mapping) to replace variants with consistent country names (e.g., 'uk' -> 'united kingdom').
Apply the mapping using .replace() .
Remove Missing/Empty Values: Handle missing or empty country entries with .dropna() and filtering.
Calculating 'days_ago':

Convert data type: Ensure the 'date_measured' column is in datetime format using pd.to_datetime().

Calculate Difference: Subtract 'date_measured' from the current date (datetime.date.today()) to find the difference in days. Convert to a new column 'days_ago'.

**Result:**

The cleaned dataset now has:

Consistent country names, aiding in accurate grouping and analysis.
A 'days_ago' column, enabling time-based exploration of income patterns.

**Usage:**

This preprocessed data is ready for downstream analysis such as:

Visualizing income trends over time across different countries.
Investigating correlations between income and time periods.
Building models to predict store income based on historical patterns and country-specific factors.
