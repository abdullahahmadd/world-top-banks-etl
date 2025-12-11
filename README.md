# ETL Pipeline: World’s Largest Banks Data Processing  
### IBM Data Engineering Specialization – Portfolio Project

This project demonstrates a complete Extract, Transform, Load (ETL) workflow using Python. The objective is to extract the top 10 largest banks by market capitalization (USD), transform the data into GBP, EUR, and INR using the provided exchange_rate.csv file, and load the processed data into both CSV and SQLite database formats. A detailed process log is also maintained throughout execution.

---

## Project Objectives
- Extract market capitalization data from an archived web source.  
- Clean and format the raw HTML table data.  
- Convert USD market capitalization values to GBP, EUR, and INR.  
- Save the transformed data into a CSV file and SQLite database.  
- Maintain process history through a structured log file (code_log.txt).  
- Present the project as a reproducible ETL pipeline.

---

## Tech Stack
- Python  
- BeautifulSoup (bs4)  
- Requests  
- Pandas  
- NumPy  
- SQLite3  
- Google Colab  
- GitHub  

---

## Repository Structure

world-top-banks-etl/
│
├── Data/
│ ├── exchange_rate.csv
│ ├── Largest_banks_data.csv
│ └── Banks.db
│
├── Notebook/
│ └── world_top_banks.ipynb
│
├── Results/
│ ├── extract.png
│ ├── transform.png
│ ├── save_csv.png
│ ├── queries_results.png
│ ├── files_log.png
│ └── etl_process_log.png
│
├── code_log.txt
└── README.md

yaml
Copy code

---

## ETL Workflow

### 1. Extract
- Scraped the necessary data from the “By market capitalization” table available on an archived Wikipedia page.  
- Cleaned text values, removed non-numeric characters, and selected the top 10 banks based on market cap in USD.

### 2. Transform
- Loaded exchange rates from exchange_rate.csv.  
- Calculated market capitalization in GBP, EUR, and INR.  
- Rounded transformed values to two decimal places.  
- Reordered DataFrame columns to match project requirements.

### 3. Load
- Saved the final DataFrame to Largest_banks_data.csv.  
- Loaded the processed data into Banks.db under the table name Largest_banks.

### 4. Logging
Each major step of the ETL workflow writes a timestamped entry to code_log.txt using the format:

YYYY-MM-DD HH:MM:SS : <message>

yaml
Copy code

---

## How to Run the Project
1. Open the notebook file located at:
Notebook/world_top_banks.ipynb

yaml
Copy code
2. Run all cells sequentially in Google Colab.  
3. Ensure exchange_rate.csv is available in the Data directory.  
4. Outputs and logs will be generated in their respective folders.

---

## Results and Evidence
All screenshots showing the extraction, transformation, CSV creation, SQL queries, and logging have been stored in the Results directory for verification.

---

## Skills Demonstrated
- Web scraping  
- Data cleaning and transformation  
- ETL pipeline development  
- SQL database creation and querying  
- Using Python libraries for automation  
- Structured logging  
- Project organization and documentation  
- Git and GitHub version control

---

## About This Project
This ETL project was completed as part of the IBM Data Engineering Specialization.  
It has been structured and documented to serve as a portfolio project sho
