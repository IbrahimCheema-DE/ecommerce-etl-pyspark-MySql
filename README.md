Set-Content README.md "# Ecommerce ETL Pipeline - PySpark & MySQL

## Project Overview
An end-to-end ETL pipeline that extracts retail sales data from MySQL, performs transformations using PySpark, and loads the results back into MySQL.

## Dataset
- **Source:** UCI Online Retail Dataset (Kaggle)
- **Records:** 980 rows
- **Features:** InvoiceNo, StockCode, Description, Quantity, InvoiceDate, UnitPrice, CustomerID, Country

## Tech Stack
- Python 3.11
- PySpark 3.5.1
- MySQL 8.0
- Jupyter Notebook
- Java 11 (OpenJDK)

## Project Structure
ecommerce-etl-pyspark-MySql/
│
├── python ecommerce_project.ipynb   # Main ETL Notebook
├── .env                             # MySQL credentials (not pushed)
├── .gitignore                       # Ignored files
└── README.md                        # Project documentation

## ETL Pipeline Steps
1. Extract - Fetch raw data from MySQL (retail_sales table)
2. Transform - Clean data, remove nulls, calculate TotalPrice
3. Analyze - Top 5 products by revenue, revenue by country
4. Load - Push transformed data back to MySQL (retail_sales_transformed table)

## Transformations Applied
- Removed null and empty CustomerID values
- Trimmed whitespace from CustomerID column
- Filtered negative quantities and zero unit prices
- Calculated TotalPrice = Quantity x UnitPrice
- Aggregated revenue by product and country

## How to Run
1. Clone the repository
   git clone https://github.com/IbrahimCheema-DE/ecommerce-etl-pyspark-MySql.git

2. Install dependencies
   pip install pyspark mysql-connector-python

3. Create .env file with your MySQL password
   MYSQL_PASSWORD=your_password_here

4. Download MySQL JDBC Driver
   Place mysql-connector-j-9.6.0.jar in project folder

5. Open Jupyter Notebook and run cells in order

## Results
- Successfully extracted 980 records from MySQL
- Cleaned and transformed data using PySpark
- Loaded transformed data back to MySQL
- Identified top performing products and countries by revenue

## Author
Ibrahim Cheema
Data Engineer | Python | PySpark | AWS | SQL | Power BI
GitHub: https://github.com/IbrahimCheema-DE
LinkedIn: https://linkedin.com/in/ibrahim-cheema-41555925a"
