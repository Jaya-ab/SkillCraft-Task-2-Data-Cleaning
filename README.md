# SkillCraft Technology – Task 2: Data Cleaning and Preparation

## Project Overview

This project was completed as part of the Data Analyst Internship at SkillCraft Technology.

The objective of this task was to load the Global Superstore dataset using Pandas, check for missing values, remove duplicate rows, convert date columns to the correct datatype, and export the cleaned dataset as a CSV file.

## Dataset

- Dataset: Global Superstore
- Rows: 51,290
- Columns: 27

## Tools & Technologies

- Python
- Pandas
- Google Colab
- CSV

## Data Cleaning Steps

### 1. Load the Dataset

The Global Superstore dataset was loaded into Google Colab using Pandas.

`df = pd.read_csv('/content/global_superstore/superstore.csv')`

### 2. Check Missing Values

Missing values were checked using `df.isnull().sum()`.

**Result:** No missing values were found.

### 3. Check Duplicate Rows

Duplicate rows were checked using `df.duplicated().sum()`.

**Result:** 0 duplicate rows were found.

### 4. Convert Date Columns

The `Order.Date` and `Ship.Date` columns were converted from object datatype to datetime format.

`df['Order.Date'] = pd.to_datetime(df['Order.Date'])`

`df['Ship.Date'] = pd.to_datetime(df['Ship.Date'])`

Both columns were successfully converted to `datetime64[ns]`.

### 5. Export Cleaned Dataset

The cleaned dataset was exported as a new CSV file.

`df.to_csv('/content/Global_Superstore_Cleaned.csv', index=False)`

## Results

- Missing Values: **0**
- Duplicate Rows: **0**
- Order.Date: **datetime64[ns]**
- Ship.Date: **datetime64[ns]**
- Cleaned CSV successfully exported

## Project Files

- `SkillCraft_Task_2_Data_Cleaning.ipynb`
- `Global_Superstore_Cleaned.csv`

## Internship

**Task 2 – Data Cleaning and Preparation**

**SkillCraft Technology Data Analyst Internship**

## Author

Jaya Sree
