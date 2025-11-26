# Final_project_Data606
Data Cleaning & Preparation: Mehreen-Proposal_visualization.rmd
read file: flights_data.csv
  Filters flights data to remove rows with missing passenger or distance values
  Creates categorical variables for distance groups, carrier types, and month names
  Generates new features like route identifiers and load factors
  Converts categorical variables to factors with specific level ordering

Missing Value Handling:
Identifies missing values (only in freight column)
Replaces NA freight values with 0

Data Quality Checks:
Converts appropriate columns to factor data types
Identifies and removes 47 duplicate rows
Cleans text columns by trimming whitespace
Validates numeric ranges to ensure no negative values exist

Final Output:
Produces a cleaned dataset ready for analysis
Creates a formatted table display of the first few rows
Confirms data quality through various validation checks
