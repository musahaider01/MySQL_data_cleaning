# MySQL_data_cleaning
Data cleaning and analysis project on MySQL

## Project Overview
This project aims to clean and analyze companies data using MySQL.  
The project includes handling duplicate rows, missing values, incorrect data, and converting dates to the correct format.

**Skills Learned / Tools Used:**
- MySQL
- Data Cleaning Techniques
- STR_TO_DATE, TRIM, CTE, Temporary Tables
- Handling NULLs and incorrect values

---

## Dataset Description
- Number of tables: One
- Number of columns: Ten

---

## Steps / Methods

### 1. Data Understanding
- Explore tables and columns.
- Check data types and identify missing or incorrect values.

### 2. Data Cleaning
- Remove duplicate rows:
```sql
SELECT DISTINCT * FROM layoffs;

• Convert dates from DD/MM/YYYY to MySQL standard format:

UPDATE layoffs
SETa before= STR_TO_DATE(TRIM(`date`), '%d/%m/%Y')
WHERE IS NOT NULL
  AND STR_TO_DATE(TRIM(`date`), '%d/%m/%Y') IS NOT NULL;

• Handle NULL or missing values:

UPDATE layoffs
SET amount = 0
WHERE amount IS NULL;

• Use Temporary Tables for complex operations


⸻

Results / Before & After
 • Total rows before cleaning: [564]
 • Total rows after cleaning: [480]

⸻

Conclusion

Through this project, the following were achieved:
 • Cleaned data from incorrect or missing values.
 • Converted dates to a standardized format for further analysis.
 • Gained advanced SQL and data cleaning skills.

⸻

