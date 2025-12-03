# Final_project_Data606
R Markdown file: https://github.com/mehreengillani/Final_project_Data606/blob/main/Mehreen-Proposal_DataCleaning.rmd
Data Loading & Initial Inspection
Loaded flight data from GitHub URL https://raw.githubusercontent.com/mehreengillani/Final_project_Data606/refs/heads/main/flights_data.csv
Checked unique values for key variables (CARRIER_GROUP, DISTANCE_GROUP, MONTH)

1. Data Cleaning & Transformation:
  Converted column names to lowercase
  Removed rows with missing passengers or distance
  Created categorical variables for distance groups and carrier types
  Generated month names, route identifiers, and load factor metrics
  Removed year column (only one value)
  Handled missing freight values by filling with 0

2. Data Quality Assurance
  Converted appropriate columns to factors
  Removed 47 duplicate rows
  Cleaned text columns by trimming whitespace
  Validated no negative values in numeric columns
  Outlier Detection & Removal
  Identified and removed invalid routes (origin = destination)

3. Filtered unrealistic values:
  Passengers ≤ 1000 (realistic capacity)
  Distance between 50-6000 miles
  Freight ≤ 1,000,000 units
  Removed flights with <20 passengers to focus on meaningful passenger operations
  
4. Final Data Validation
  Verified no missing values (except minor freight NAs)
  Confirmed no duplicates remain
  Checked realistic data ranges and factor level consistency
  Saved cleaned dataset as RDS file for analysis
  
Result: Cleaned dataset with 32,476 passenger flights ready for robust analysis.

Data visualization: rmd file visualization_FP_606.Rmd
statistical analysis file Statistical_analysis_finalProject_606.Rmd
