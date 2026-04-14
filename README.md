# UK Road Accident Intelligence Dashboard

## Project Overview
Working as a Data Insights Analyst at INRIX, I create incident 
reports daily for road disruptions across North America and the UK. 
After 15 months in the role I noticed the same locations appearing 
repeatedly in accident reports. This project investigates why — using 
publicly available UK government data to identify structural patterns 
behind repeat accident hotspots.

## Business Questions Answered
1. Where are the repeat accident hotspot locations across the UK?
2. Are accidents caused by road conditions or structural road design?
3. When do accidents at hotspot locations occur — time of day and season?
4. What type of vehicle manoeuvres are involved in repeat accidents?
5. Which locations should be prioritised for intervention and why?

## Key Findings
- **19,846 repeat accident hotspot locations** identified across the 
  UK between 2021 and 2023
- **84% of repeat hotspot accidents** occurred in fine weather on dry 
  roads in daylight — pointing to road design as the primary cause, 
  not weather or driver error
- **Junction-related problems** account for the majority of repeat 
  hotspot locations — with turning movements being the most common 
  accident manoeuvre
- **Night-time** is the dominant accident period across most hotspot 
  locations despite lower traffic volumes
- **London and the Midlands** contain the highest concentration of 
  high-severity repeat hotspots

## Technical Stack
- **SQL (SQLite)** — Data cleaning, multi-table joins, CTEs, window 
  functions, CASE WHEN logic, CREATE VIEW
- **Python (Pandas)** — File combining and data export automation
- **Power BI** — 4-page interactive dashboard with geospatial mapping, 
  drillthrough analysis, DAX measures, and conditional formatting
- **Excel** — Initial data profiling and column pruning

## Data Source
UK Department for Transport — STATS19 Road Safety Data 2021–2023
- 311,349 collision records
- 396,666 casualty records  
- 569,803 vehicle records
- Source: https://www.gov.uk/government/statistical-data-sets/road-safety-open-data

## Dashboard
View the live interactive dashboard here : (https://app.powerbi.com/groups/me/reports/0b380fbe-a94d-44a4-a14a-c9ab27a6246b/0d2232e90ab9d465dcf2?experience=power-bi)

## Repository Contents
- `queries.sql` — All SQL queries used in the analysis including 
  the master hotspot view
- `combine_files.py` — Python script used to combine yearly data files
- `screenshots/` — Dashboard screenshots

## Project Structure
The analysis is built around a master SQLite view combining all 
three STATS19 tables using CTEs. The view automatically classifies 
each hotspot location by type and generates a recommended intervention 
using CASE WHEN logic — making it directly actionable for transport 
authorities, insurers, and logistics companies.
