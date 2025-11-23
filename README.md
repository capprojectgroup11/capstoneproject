# Forecasting Alberta Electricity Load and Generation Mix
### Capstone Project – St. Clair College (DAB 322)
### Capstone Group 11

## 📌 Project Overview
This project analyzes Alberta’s electricity system using official AESO open data. It focuses on historical electricity demand (load), generation by fuel type, and regional population trends from 2011–2025. The analysis includes a full Python cleaning pipeline (`CAPSTONE_PY.ipynb`) and multi-page Tableau dashboards.

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
All raw datasets were downloaded from the above sources and cleaned using `CAPSTONE_PY.ipynb`.  
The notebook includes:
- Duplicate timestamp removal  
- Missing value checks  
- Extraction of time features (year, month, hour)  
- Standardized column names  
- Calculation of `TOTAL_LOAD` from AREA columns  
- Merging load, generation, and population datasets  
- Exporting cleaned CSV files for Tableau  

## 📊 Tableau Dashboards
Dashboards include:
- Total Load Trends  
- Regional Comparison  
- Generation Mix by Fuel Type  
- Population vs Load  
- Electric Surge (95th percentile events)  

## 🤖 Optional Forecasting
Prototype forecasting models explored:
- LSTM  
- GRU  
- Temporal Fusion Transformer  

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
Antash  
Rajdeep  
Drumil  
Niti  
Riya  

Instructor: Prof. Manjari Maheshwari
