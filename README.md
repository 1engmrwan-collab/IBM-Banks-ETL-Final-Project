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
