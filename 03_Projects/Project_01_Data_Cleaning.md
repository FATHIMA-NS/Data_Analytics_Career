- **Title:** Identifying and Resolving Dataset Inconsistencies
    
- **Date:** 18-07-2026
    
- **Dataset Source:** [Kaggle: Dirty Dataset for Practice](https://www.kaggle.com/datasets/amruthayenikonda/dirty-dataset-to-practice-data-cleaning)
    
- **Tools Used:** Google Sheets
    

### 1. The Business Task

The objective of this project was to:

- **Data Cleaning:** Standardize raw dataset formatting, remove citation noise, and resolve data inconsistencies to ensure high-quality analysis.
    
- **Performance Analysis:** Identify the top-performing tours based on actual gross revenue and determine industry trends.
    

### 2. Issues Identified (The "Before")

- **Issue 1:** The 'Rank' column contained duplicate values (specifically Rank 7), necessitating an investigation to distinguish between data errors and valid ties.
    
- **Issue 2:** High volume of missing values in the 'Peak' (11) and 'All Time Peak' (14) columns.
    
- **Issue 3:** Inconsistent formatting in 'Peak', 'All Time Peak', and 'Actual gross' columns, with numeric values mixed with citation markers (e.g., `7[2]` and `$229,100,000[b]`).
    

### 3. Actions Taken (The "Process")

- **Step 1:** Cleaned 'Peak' and 'All Time Peak' columns by removing bracketed citation markers using Regular Expressions (`\[.*\]`).
    
- **Step 2:** Cleaned the 'Actual gross' column by removing citation markers and applying proper currency/numeric formatting.
    
- **Step 3:** Investigated the Rank 7 entries and confirmed they represent a valid tie between two distinct tours rather than a duplicate record.
    
- **Step 4:** Standardized missing values by labeling them as 'NA' to maintain dataset integrity.
    
- **Step 5:** Verified the numeric data type of the 'Actual gross' column by successfully calculating the average.
    
- **Step 6:** Performed a range-wide sort of the entire dataset based on the 'Actual gross' column in descending order to identify top-performing tours.
    

### 4. Results (The "After")

- **Insight:** The average gross for the tours in this dataset is $287,950,903.25. The top-performing tour is 'The Eras Tour' with a gross of $780,000,000.
    

### 5. Key Learnings

- Developed the ability to distinguish between actual data duplicates and valid statistical ties through contextual investigation.
    
- Gained proficiency in using Regular Expressions (Regex) to clean noise from unstructured datasets.
    
- Strengthened skills in data preparation, sorting, and exploratory analysis to uncover meaningful insights.