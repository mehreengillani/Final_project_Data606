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

Data visualization: rmd file: visualization_FP_606.Rmd
The investigation employs extensive univariate and multivariate data visualization techniques to uncover insights about:

1.  Passenger distribution and travel demand fluctuations
2.  Flight frequency patterns across major routes
3.  Origin-destination dynamics and popular travel corridors
4.  Carrier performance comparisons across three categories: Major, National, and Regional carriers

Statsitical Analysis: rmd file: Statistical_analysis_FP_606.Rmd

Research Questions & Methodology

1. Seasonal Flight Distribution

I tested whether flight frequencies are uniformly distributed across months using a chi‑square goodness‑of‑fit test. 
Our analysis provides strong evidence against equal monthly distribution (χ² = 155.54, df = 6, p ≈ 0), indicating airlines strategically adjust schedules in response to seasonal travel patterns.

2. Carrier‑Type Performance
evaluated differences in flight frequencies and passenger volumes across three carrier classifications—major, national, and regional—using:

Chi‑square tests for flight frequency comparisons
ANOVA for passenger volume analysis

Performed Linear regression for passengers and flight 

Statstatistical analysis file Statistical_analysis_finalProject_606.Rmd

