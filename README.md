# ETL Pipeline: World’s Largest Banks Data Processing  
### IBM Data Engineering Specialization – Portfolio Project

![Visitors](https://visitor-badge.laobi.icu/badge?page_id=abdullahahmadd.world-top-banks-etl)
![ETL](https://img.shields.io/badge/ETL%20Pipeline-purple)
![Web Scraping](https://img.shields.io/badge/Web%20Scraping-darkred)
![Python](https://img.shields.io/badge/Python-blue)
![Google Colab](https://img.shields.io/badge/Google%20Colab-yellow)
![Pandas](https://img.shields.io/badge/Pandas-green)
![NumPy](https://img.shields.io/badge/NumPy-orange)
![BeautifulSoup](https://img.shields.io/badge/BeautifulSoup-red)
![SQLite](https://img.shields.io/badge/SQLite-lightgrey)

---

This project demonstrates a complete Extract, Transform, Load (ETL) workflow using Python. The goal is to extract the top 10 largest banks by market capitalization (USD), transform the data into GBP, EUR, and INR using the provided `exchange_rate.csv`, and load the processed data into both CSV and SQLite database formats. A detailed process log is also maintained throughout execution.

---

## Table of Contents
1. [Project Objectives](#project-objectives)  
2. [Tools & Technologies](#tools--technologies)  
3. [Libraries Used](#libraries-used)
4. [Skills Demonstrated](#skills-demonstrated)     
5. [How to Run the Project](#how-to-run-the-project)  
6. [Results](#results)  
7. [ETL Workflow](#etl-workflow)
8. [About This Project](#about-this-project)

---

## Project Objectives
- Extract market capitalization data from an archived web source.  
- Clean and structure the raw data into a pandas DataFrame.  
- Convert USD market capitalization into GBP, EUR, and INR.  
- Save transformed data into a CSV file and SQLite database.  
- Log all major steps using a structured log file (`code_log.txt`).  
- Provide a clean, reproducible ETL workflow.
---

## Tools & Technologies
- ETL Process
- Google Colab  
- Python  
- SQLite  

---

## Libraries Used
- `requests`  
- `BeautifulSoup (bs4)`  
- `pandas`  
- `numpy`  
- `sqlite3`  
- `datetime`  

---

## Skills Demonstrated
- Web scraping using BeautifulSoup  
- Data cleaning and transformation with pandas  
- ETL workflow creation  
- SQL database loading and querying  
- Structured logging of workflow events  

---

## ETL Workflow

### 1. Extract
- Scraped the “By market capitalization” table from the archived Wikipedia page.  
- Cleaned values and extracted the top 10 largest banks by USD market cap.

### 2. Transform
- Loaded exchange rates from `exchange_rate.csv`.  
- Calculated market capitalization in GBP, EUR, and INR.  
- Rounded transformed values to two decimal places.  
- Reordered DataFrame columns to match project requirements.

### 3. Load
- Saved the final DataFrame to `Largest_banks_data.csv`.  
- Loaded the processed data into `Banks.db` under the table name `Largest_banks`.

### 4. Logging
All major steps write timestamped entries into `code_log.txt` using:
YYYY-MM-DD HH:MM:SS : <message>

---

## How to Run the Project
1. Open the notebook located at:  
Notebook/world_top_banks.ipynb
2. Run all cells in Google Colab or Jupyter Notebook.  
3. Ensure `exchange_rate.csv` is present in the Data directory.  
4. The output CSV, database, and logs will be recreated upon execution.

---

## SQL Analysis Results  
All SQL outputs are stored in the `Cylistic_analysis_results/` folder.

| 1. Total Rows Loaded |
|----------------------|
| ![Total Rows](Cylistic_analysis_results/total_rows_sql.png) |
| Shows the number of successfully imported rows in MySQL after loading the dataset. |

---

| 2. Missing Values Check |
|-------------------------|
| ![Missing Values](Cylistic_analysis_results/missing_values_sql.png) |
| Displays the count of missing or NULL values across all dataset columns. |

---

| 3. First 10 Rows Preview |
|--------------------------|
| ![Preview 10 Rows](Cylistic_analysis_results/10_rows_sql.png) |
| Shows a preview of the first 10 rows to verify data formatting and integrity. |

---

| 4. Average Ride Duration (SQL) |
|--------------------------------|
| ![Average Ride Duration](Cylistic_analysis_results/avg_ride_minutes_sql.png) |
| Calculates the mean ride duration across all rides using SQL aggregate functions. |

---

| 5. Maximum Ride Duration |
|---------------------------|
| ![Max Ride Duration](Cylistic_analysis_results/max_ride_minutes.png) |
| Identifies the longest ride duration recorded in the dataset. |

---

| 6. Ride Length (Seconds & Minutes) |
|------------------------------------|
| ![Ride Length in Seconds](Cylistic_analysis_results/ride_length_and_secs_sql.png) |
| Shows computed ride lengths converted into seconds and minutes for deeper analysis. |

---

| 7. Most Active Day of Week |
|-----------------------------|
| ![Most Active Day](Cylistic_analysis_results/hightest_day_of_week_sql.png) |
| Reveals which weekday had the highest number of total rides. |

---

| 8. Avg Ride Duration — Member vs Casual |
|-----------------------------------------|
| ![Avg Ride Duration User Type](Cylistic_analysis_results/member_casual_avg_ride_mints_Sql.png) |
| Compares average ride duration between casual riders and annual members. |

---

| 9. Total Rides — Member vs Casual |
|-----------------------------------|
| ![Total Rides User Type](Cylistic_analysis_results/member_casual_total_rides_sql.png) |
| Displays total trip counts for each rider category (member vs casual). |

---

| 10. Hourly Ride Distribution |
|------------------------------|
| ![Hourly Ride Distribution](Cylistic_analysis_results/hightest_rides_by_hour_sql.png) |
| Shows peak riding hours, indicating commuting and leisure time patterns. |

---

| 11. Monthly Ride Distribution |
|-------------------------------|
| ![Monthly Ride Distribution](Cylistic_analysis_results/hightest_rides_by_month_sql.png) |
| Displays the number of rides per month to highlight seasonal trends. |

---

## About This Project
This ETL pipeline was completed as part of the IBM Data Engineering Specialization.  
The project has been structured, documented, and uploaded to GitHub as a portfolio project showcasing practical data engineering skills.
