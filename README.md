# Data Cleaning and Preparation

## Overview
This notebook (`Task 1.ipynb`) demonstrates the process of cleaning a raw dataset downloaded from Kaggle. The primary goal is to prepare the data for further analysis by performing several cleaning operations such as dropping unnecessary columns, removing duplicates, standardizing text, converting date fields, and renaming column headers.

## Steps Performed

### 1. Downloading and Loading the Dataset
- **Dataset Download:** Utilized the `kagglehub` API to download the dataset.
- **Data Loading:** Loaded the dataset into a pandas DataFrame for processing.

### 2. Dropping Unnecessary Columns
- **Removed Columns:** Dropped columns like `ADDRESSLINE1`, `ADDRESSLINE2`, and `TERRITORY` to focus on relevant data.

### 3. Removing Duplicate Records
- **Duplicate Identification and Removal:** 
  - Identified duplicate rows using `df.duplicated()`.
  - Removed duplicates with `df.drop_duplicates()` to ensure data integrity.

### 4. Standardizing Text Fields
- **Text Cleaning:** 
  - Converted text to lowercase using `.str.lower()`.
  - Stripped leading and trailing whitespace using `.str.strip()`.
  - Applied custom mappings to standardize entries (e.g., for gender or country names).

### 5. Converting Columns to Datetime
- **Date Conversion:** 
  - Converted date columns to datetime objects with `pd.to_datetime()`.
  - This allowed for proper date handling and time-based operations.

### 6. Renaming Column Headers
- **Header Standardization:** 
  - Renamed columns to be uniform by converting them to lowercase, stripping extra spaces, and replacing spaces with underscores.
  - For example, `"Address Line 1"` became `address_line_1`.

### 7. Exporting the Cleaned Dataset
- **Export to CSV:** 
  - Saved the cleaned DataFrame to a CSV file using:
    ```python
    df.to_csv('cleaned_data.csv', index=False)
    ```
  - This export makes the dataset ready for future analysis and sharing.

## Dependencies
- Python 3.x
- Pandas
- Kagglehub API

## How to Run the Notebook
1. **Install Required Libraries:**  
   Use pip to install the necessary libraries:
   ```bash
   pip install pandas kagglehub
