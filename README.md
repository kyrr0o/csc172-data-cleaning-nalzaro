# Data Cleaning with AI Support

## Student Information
- Name: Kaycee Nalzaro  
- Course Year: BSCS 4
- Date: 2025-09-26

## Dataset
- Source: [Titanic - Kaggle](https://www.kaggle.com/competitions/titanic/data)
- Name: Titanic Passenger Dataset

## Issues found
- Missing values: `Age`, `Embarked` (and many in `Cabin`, though column not present in our raw CSV version).
- Duplicates: some duplicate rows found.
- Inconsistencies: `Name` not standardized, `Sex` values in mixed case.
- Outliers: extreme values in `Age` and `Fare`.

## Cleaning steps
1. Filled `Age` with the median.
2. Filled `Embarked` with the mode.
3. Dropped `Cabin` column if present (mine was already absent).
4. Removed duplicate rows.
5. Standardized `Name` (title case) and `Sex` (lowercase).
6. Detected and removed Age outliers using IQR method.

## AI prompts used
- **Prompt 1:**  
  "Provide step-by-step guidance for a data cleaning activity using the Titanic dataset. The instructions should include how to check for missing values, handle duplicates, standardize data formats, and detect outliers using Python (Pandas)."

- **Assistant response excerpt:**  
  "You can start by loading the raw dataset and running `df.info()` and `df.describe()` to explore the structure. Next, handle missing values by filling numeric columns (e.g., Age) with the median, categorical columns (e.g., Embarked) with the mode, drop or ignore the Cabin column if missing, remove duplicates, and standardize text fields such as Name and Sex."

## Results
- Rows before: (891, 12) or 891 rows
- Rows after: (825, 11) or 825 rows

## Video
- [Unlisted YouTube / Google Drive link here]
