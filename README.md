# 📊 SQL Project — Data Cleaning (World Layoffs Dataset)

## 📌 Project Overview
This project focuses on **cleaning and preparing real‑world layoff data** from the [2022 World Layoffs dataset on Kaggle](https://www.kaggle.com/datasets/swaptr/layoffs-2022).  
The goal was to transform raw, messy data into a **clean, analysis‑ready format** using MySQL.

---

## 🎯 Objectives
1. Identify and **remove duplicates** to ensure data integrity.
2. **Standardize data** (industry names, country names, date formats).
3. **Handle missing values** logically and consistently.
4. Remove **irrelevant rows/columns** that do not contribute to analysis.

---

## 🛠️ Skills Demonstrated
- **Data Cleaning Workflow**
  - Created a **staging table** to protect raw data.
  - Removed duplicates using `ROW_NUMBER()` with `PARTITION BY`.
  - Standardized inconsistent values (`Crypto`, `United States.` → `United States`).
  - Fixed date formats using `STR_TO_DATE()` and `ALTER TABLE`.
  - Updated missing industry values via **self‑join imputation**.
- **String Functions**
  - `TRIM()`, `LOWER()`, `UPPER()`, `SUBSTRING()`
- **Window Functions**
  - `ROW_NUMBER()` for identifying duplicates.
- **DDL/DML**
  - `ALTER TABLE`, `DELETE`, `UPDATE`, `INSERT`
- **Best Practices**
  - Worked in a **staging environment** before making permanent changes.
  - Followed a repeatable cleaning process.

---

## 📂 Workflow Summary
1. **Create Staging Table**
   ```sql
   CREATE TABLE layoffs_staging LIKE layoffs;
   INSERT INTO layoffs_staging SELECT * FROM layoffs;
