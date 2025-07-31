SQL Portfolio – Data Cleaning & Exploratory Data Analysis
This repository contains two SQL projects demonstrating real-world data cleaning and exploratory analysis skills using MySQL. The projects are based on the Global Layoffs Dataset from Kaggle.

Project 1 – Data Cleaning
Objective:
Prepare the raw dataset for accurate analysis by removing duplicates, standardizing data formats, handling missing values, and fixing inconsistencies.

Key Steps:

Created a staging table to preserve raw data and work on a clean copy.

Removed duplicates using ROW_NUMBER() and CTEs.

Standardized data:

Unified inconsistent industry names (e.g., “CryptoCurrency” → “Crypto”).

Removed trailing punctuation from country names.

Converted date strings to proper DATE format.

Filled missing values using self-joins where other rows had the correct data.

Removed unusable rows where no layoff data was available.

SQL Concepts Used:

ROW_NUMBER() and PARTITION BY for duplicate detection

UPDATE with JOIN to fill missing values

String cleaning functions: TRIM, STR_TO_DATE

Conditional DELETE for unusable rows

Project 2 – Exploratory Data Analysis (EDA)
Objective:
Identify patterns, trends, and key insights in the cleaned layoffs dataset.

Key Analysis Examples:

Largest single-day layoffs by company

Companies with the most total layoffs

Layoffs by location and country

Industries with the highest layoffs

Funding stages most affected

Year-over-year ranking of companies with the most layoffs (DENSE_RANK())

Monthly layoffs and rolling totals using window functions

SQL Concepts Used:

GROUP BY and aggregate functions (SUM, MAX, MIN)

DENSE_RANK() for yearly rankings

CTEs for multi-step analysis

Window functions for rolling totals

Skills Demonstrated
Data cleaning: removing duplicates, standardizing formats, filling nulls

Data analysis: aggregations, rankings, time series analysis

Advanced SQL: CTEs, window functions, subqueries

Real-world dataset handling: preparing messy public datasets for analysis

Repository Structure
pgsql
Copy
Edit
/SQL-Portfolio
│── Data_Cleaning.sql      # Full SQL script for data cleaning
│── EDA.sql                # Full SQL script for exploratory analysis
│── README.md              # Project documentation
Dataset
Name: Layoffs 2022

Source: Kaggle – Global Layoffs Dataset

Description: Records of global layoffs across industries, locations, and company stages.

Insights & Findings
Startups, especially in crypto and tech, were hit hardest.

Several companies, including Quibi and BritishVolt, shut down completely despite raising billions.

The United States had the highest total layoffs globally.

Layoffs increased sharply in 2022, particularly in later funding stages.
