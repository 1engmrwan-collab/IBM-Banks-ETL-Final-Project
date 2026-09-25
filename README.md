IBM Data Engineering Final Project
- Extract top banks data
- Bronze Layer
- Silver Transformation
- Gold Layer
- Currency conversion
- SQLite database
- SQL queries
- Logging

- _______________________________________________________________________________________________________________
- # IBM Banks ETL Final Project

This project is my final ETL project from the IBM Data Engineering course.

The main idea of the project is to build a simple ETL pipeline that extracts data about the world's largest banks, transforms the data using exchange rates, and then loads the final result into CSV files and a SQLite database.

I also organized the project using Bronze, Silver, and Gold layers to make the data flow clearer and closer to a real Data Engineering workflow.

---

## Project Workflow

The project follows this flow:

Source Data  
↓  
Bronze Layer  
↓  
Silver Layer  
↓  
Gold Layer  
↓  
SQLite Database  
↓  
SQL Queries  
↓  
Logging

---

## Bronze Layer

The Bronze Layer stores the raw extracted data before applying any transformation.

File:

```text
data/bronze/banks_raw.csv

The dataset contains:

Bank name
Market capitalization in USD
Silver Layer

In the Silver Layer, the data is transformed and prepared for further use.

The market capitalization is converted from USD to:

GBP
EUR
INR

The values are rounded to two decimal places.

File:

data/silver/banks_transformed.csv
Gold Layer

The Gold Layer contains the final dataset ready for analysis or reporting.

File:

data/gold/Largest_banks_data.csv

Final columns:

Name
MC_USD_Billion
MC_GBP_Billion
MC_EUR_Billion
MC_INR_Billion
Database

The final dataset is also loaded into a SQLite database.

Database:

Banks.db

Table:

Largest_banks

The project runs SQL queries to:

Display all bank records
Calculate the average market capitalization in GBP
Display the names of the top 5 banks
Logging

A logging system is included to track the main ETL stages.

Log file:

logs/code_log.txt

The log records stages such as:

ETL process started
Data extraction completed
Transformation completed
Data loaded into the database
SQL queries executed
Database connection closed
Project Structure
IBM_Banks_ETL_Project/
│
├── data/
│   ├── bronze/
│   │   └── banks_raw.csv
│   │
│   ├── silver/
│   │   └── banks_transformed.csv
│   │
│   └── gold/
│       └── Largest_banks_data.csv
│
├── logs/
│   └── code_log.txt
│
├── banks_project.py
├── exchange_rate.csv
├── Largest_banks_data.csv
├── Banks.db
├── requirements.txt
└── README.md
Technologies Used
Python
Pandas
Requests
SQLite
HTML Table Extraction
ETL
SQL
Logging
Medallion Architecture
What I Learned

Through this project, I practiced how to build a complete ETL workflow from start to finish.

I learned how to:

Extract data from a web source
Work with Pandas DataFrames
Clean and transform data
Convert financial values using exchange rates
Organize data using Bronze, Silver, and Gold layers
Save data to CSV files
Load data into a SQLite database
Run SQL queries
Add logging to track the ETL process

This project helped me understand how the different stages of a Data Engineering pipeline work together in one complete workflow.
