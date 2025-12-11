ETL Pipeline: World’s Largest Banks Data Processing
IBM Data Engineering Specialization – Portfolio Project

This project demonstrates a complete Extract, Transform, Load (ETL) workflow using Python, web scraping, data cleaning, currency conversion, structured logging, and database loading.
The goal is to extract the top 10 largest banks in the world by market capitalization (USD), transform the values into GBP, EUR, and INR, and load the processed data into CSV and a SQLite database.

📌 Project Objectives

Extract market capitalization data for the world’s top banks from an archived web source.

Clean and structure the raw data into a pandas DataFrame.

Convert market capitalization from USD → GBP, EUR, INR using exchange_rate.csv.

Load the final dataset into:

A CSV file

A SQLite database (Banks.db)

Maintain execution history using a detailed code_log.txt.

Present the project as a real-world portfolio ETL pipeline.

🛠 Tech Stack

Python

BeautifulSoup (bs4) — Web scraping

Requests — Data extraction

Pandas / NumPy — Data transformation

SQLite3 — Database creation & loading

Google Colab — Development environment

Markdown + GitHub — Documentation & portfolio presentation

📂 Repository Structure
world-top-banks-etl/
│
├── Data/
│   ├── exchange_rate.csv
│   ├── Largest_banks_data.csv
│   └── Banks.db
│
├── Notebook/
│   └── world_top_banks.ipynb
│
├── Results/
│   ├── extract.png
│   ├── transform.png
│   ├── save_csv.png
│   ├── queries_results.png
│   ├── files_log.png
│   └── etl_process_log.png
│
├── code_log.txt
└── README.md

🔄 ETL Workflow Overview
1️⃣ Extract

Scrape table under "By market capitalization" from the archived Wikipedia page.

Clean text, remove footnotes, parse numbers, and select top 10 rows.

2️⃣ Transform

Load exchange rate CSV

Convert MC_USD_Billion to:

MC_GBP_Billion

MC_EUR_Billion

MC_INR_Billion

Round values to 2 decimal places

Reorder final columns

3️⃣ Load

Save transformed dataset to Largest_banks_data.csv

Load final table into Banks.db under table name Largest_banks

4️⃣ Logging

Each major step writes an entry to code_log.txt in the format:

YYYY-MM-DD HH:MM:SS : <status message>

▶️ How to Run the Project

Open the notebook:

Notebook/world_top_banks.ipynb


Run all cells top to bottom in Google Colab.

Make sure exchange_rate.csv is located inside the Data folder.

Outputs will appear in the Data folder and logs in the repo root.

📸 Results & Screenshots

Screenshots of extraction, transformation, saving, SQL outputs, and logs are available in the Results/ directory.

These help demonstrate work for peer review and portfolio presentation.

📘 Key Skills Demonstrated

Web scraping using BeautifulSoup

ETL Pipeline development

Data cleaning & transformation

Working with external CSV sources

SQL database creation & loading

Structured logging for ETL processes

Organizing a project for real-world portfolios

Git & GitHub best practices

🎯 About This Project

This project was completed as part of the IBM Data Engineering Specialization and uploaded to GitHub as a portfolio project to demonstrate practical ETL development capability using Python and SQL.

⭐ If you like this project

Feel free to star ⭐ the repo or connect with me on LinkedIn!
