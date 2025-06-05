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
```sql
SELECT SUM(Value) FROM milk_production WHERE Year = 2023;
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


