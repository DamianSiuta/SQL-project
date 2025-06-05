# SQL Production Analysis Project

## Overview
This repository contains SQL queries and dataset analyses for various production data, including **milk, coffee, honey, cheese, eggs, and yogurt**. The project provides structured queries to derive key statistics and insights from production datasets.

## Contents
### **SQL Queries**
The repository includes structured queries for:
- **Aggregations** (SUM, AVG, MAX)
- **Filtering by Year or Category**
- **State-based Production Lookups**
- **JOIN Operations**
- **Data Formatting and Type Conversion**

### **Example SQL Queries**
#### 1️⃣ **Total Milk Production for 2023**
#### ✅ Counting states with significant cheese production in April 2023
```
SELECT count(distinct State_ANSI) AS count_states 
FROM cheese_production 
WHERE Year = 2023 AND Period = 'APR' AND Value > 100000000;
```

✅ Check if Delaware had cheese production in April 2023
```
SELECT CASE WHEN EXISTS (
    SELECT 1 FROM cheese_production 
    WHERE Year = 2023 AND Period = 'Apr' 
    AND State_ANSI = (SELECT State_ANSI FROM state_lookup WHERE State = 'Delaware')
) THEN 'Yes' ELSE 'No' END AS Delaware_Cheese_Production;
```
```
Results Summary
| Query | Answer | 
| Milk Production in 2023 | 91,812,000,000 | 
| Coffee Production in 2015 | 6,600,000 | 
| Average Honey Production (2022) | 3,133,275 | 
| State ANSI for Iowa | 19 | 
| Highest Yogurt Production (2022) | 793,256,000 | 
| Delaware Cheese Production (Apr 2023) | No | 
| Number of states with significant cheese production | 14 | 
| Count of states with no milk production in 2023 | 26 | 
```

How to Run
To execute these queries:
- Clone the repository:
git clone https://github.com/DamianSiuta/SQL-Production.git
- Navigate to the SQL files and execute them in your database:
cd SQL-Production
- Load SQL queries:
SOURCE 1part_final_project.sql;
SOURCE 2part_final_project.sql;


Contributing
Feel free to fork this repository, submit pull requests, or suggest improvements.
License
This project is released under the MIT License.

Happy querying! 🚀



