# Forecasting Alberta Electricity Load and Generation Mix
### Capstone Project – DAB 322 (Fall 2025)
### Program: Data Analytics for Business – St. Clair College
### Team: Capstone Group 11
### Instructor: Prof. Manjari Maheshwari
### Tools Used: Python, Pandas, Matplotlib, Seaborn, Excel, Tableau

## 📌 Project Overview
This project analyzes Alberta’s electricity system using official open data from the Alberta Electric System Operator (AESO) and regional population data.
The aim is to understand how electricity demand (load) and electricity supply (generation by fuel type) have changed over time, and how they are influenced by season, time of day, region, and population growth.
The project also identifies “surge hours” — the top 5% of highest electricity demand — to highlight periods of extreme system pressure.

The final output consists of:
A complete Python-based data cleaning and analysis pipeline
Multiple interactive Tableau dashboards
Key insights about demand, generation, and population trends in Alberta

## 📂 Datasets Used

### 1. AESO Hourly Load by Area and Region  
**Title:** Hourly Load by Area and Region – AESO  
**Link & Access:** https://www.aeso.ca/market/market-and-system-reporting/data-requests/hourly-load-by-area-and-region  

### 2. AESO Historical Generation Data  
**Title:** Historical Generation Data – AESO  
**Link & Access:** https://www.aeso.ca/market/market-and-system-reporting/data-requests/historical-generation-data  

### 3. Alberta Population Dataset  
**Title:** Statistics Canada – Alberta Population Estimates  
**Link & Access:** https://www150.statcan.gc.ca/6f7c1265-c1d1-4e3c-a85b-cab3feb4fc6a  

## 🧹 Data Cleaning & Processing
The data preparation followed a two-stage process:

### 1. Initial Preparation in Excel
Before moving to Python, the raw files were first reviewed in Excel. During this step, I:
Merged some related files into a single dataset
Fixed basic formatting issues
Checked and adjusted column names
Removed clearly empty or irrelevant rows
This step was only to prepare the data for smooth loading into Python.

### 2. Main Cleaning & Processing in Python

The main data preparation and analysis was done in Python using Pandas and implemented in the file:CAPSTONE_PY.ipynb

Key steps in Python included:
Removing duplicate and missing timestamps
Standardizing column names and formats
Creating TOTAL_LOAD from AREA columns

Extracting time features:
YEAR, MONTH, HOUR, DAY_OF_WEEK, SEASON
Cleaning negative or invalid generation values
Pivoting generation data to wide format (one column per fuel type)
Merging load and generation by timestamp
Identifying surge hours using the 95th percentile
(≈ 9,220 MW, top 5% of hours)
Aggregating yearly population and total generation
Calculating correlation between population and generation

All major computation, logic, and analysis was done in Python. Excel was only used for light preparation and final verification.

## Final Cleaned Output Files (Used in Tableau)

These are the main files generated from Python and used in Tableau:
AESO_Load_2011_2024_Final.csv
AESO_Generation_By_Fuel_2020_2025_Clean.csv (long format)
AESO_Generation_By_Fuel_2020_2025_Wide.csv (wide format)
AESO_Load_Generation_2020_2024_with_Surge.csv
Generation_Population_Yearly_2020_2024.csv

## 📊 Tableau Dashboards
ableau Dashboards
Using these files, the following dashboards were created:
Long-Term Load Trends (2011–2024)
Regional Electricity Load Comparison
Generation Mix by Fuel Type
Population vs Generation Growth
Surge Hours Analysis (Top 5%)

These dashboards clearly show:
When electricity demand is highest
Which regions consume more power
Which fuels dominate Alberta’s energy mix
How population growth relates to generation demand

## 🤖 Optional Forecasting
Prototype forecasting models explored:
- LSTM  
- GRU  
   

## 📁 Repository Structure
```
/data
   /raw
   /cleaned
/code
   CAPSTONE_PY.ipynb
/tableau
   dashboards.twbx
/docs
   project_report.pdf
README.md
```

## 👥 Team – Capstone Group 11
Team – Capstone Group 11

Antash Devani
Rajdeepsinh Gohil
Drumil Trivedi
Niti Dangri
Riya Patel

Course: DAB 322 – Capstone Project 1
Instructor: Prof. Manjari Maheshwari
Institution: St. Clair College 
