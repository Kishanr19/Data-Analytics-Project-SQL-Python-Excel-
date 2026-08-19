Data-Analytics-Project-SQL-Python-Excel

A collection of analyst-style projects spanning PostgreSQL, Python, Excel, and Tableau. Each project is built around a specific business question — from bike store sales and inventory, to employee attrition, to options market data — and demonstrates a different stage of the analytics workflow, from database design through modeling to dashboarding.

Notable Features
Relational database design and schema management for a retail sales dataset (PostgreSQL)
20+ analytical SQL queries covering revenue, customers, inventory, and staff performance
An automated Python pipeline that retrieves and stores options market data via API
A logistic regression model predicting employee churn, with full EDA and cross-validation
Excel-based statistical testing and pivot-table analysis of retail margins
Interactive Excel and Tableau dashboards for property sales and retail performance
Setup and Running Instructions
Prerequisites
PostgreSQL (for the SQL and Python pipeline projects)
Python 3.x with pandas, SQLAlchemy, and requests installed
Microsoft Excel (2016 or later recommended, for pivot tables and slicers)
Jupyter Notebook or JupyterLab (to run the .ipynb files)
Tableau Public account (optional, only needed to edit the Tableau dashboards — viewing requires no account)
Running the SQL Projects
Open BicyclesDB.sql in a PostgreSQL client (e.g., pgAdmin or psql) to build the database schema
Load the CSV files from the Bike Store Data/ folder into the corresponding tables
Run Bike Store Sales Analysis.sql to execute the analysis queries
Running the Python Projects
Open the relevant .ipynb file in Jupyter
Install any missing dependencies listed at the top of the notebook
For the S&P 500 pipeline, a Tradier Sandbox API key is required and a local PostgreSQL instance must be running
Run all cells in order
Opening the Excel and Tableau Projects
Excel files can be opened directly; pivot tables and slicers are interactive out of the box
Tableau dashboards are hosted externally and viewable via the links below — no local setup required
Project Structure
Data-Analysis-Portfolio/
├── BicyclesDB.sql                              # Database schema for bike store data
├── Bike Store Sales Analysis.sql               # Analytical SQL queries
├── Bike Store Data/                             # Source CSVs (production + sales)
├── S&P 500 Database Pipeline.ipynb             # Options data pipeline notebook
├── SPY_ERD.png                                  # ERD for the SPY database
├── Salifort Motors - Employee Churn Prediction.ipynb  # Churn prediction notebook
├── Adidas US Sales EDA.xlsx                    # Excel EDA + hypothesis testing
├── 2022 Milwaukee Property Sales Dashboard.xlsx # Excel dashboard
├── 2022 Milwaukee Property Sales Dashboard.pdf  # Static preview of the dashboard
├── query results/                               # Exported outputs from SQL queries
└── README.md                                    # This documentation file
Project Breakdown
PostgreSQL

BicyclesDB.sql — Builds the relational schema for a bike retailer's sales and inventory system. Skills: database design, schema management, table alteration, PSQL commands

Bike Store Sales Analysis.sql — Queries covering order processing, revenue, customer behavior, inventory, and staff performance. Skills: subqueries, aggregation, joins, filtering, grouping ERD: DrawSQL Diagram

Python

S&P 500 Database Pipeline.ipynb — Pulls SPY options data for a chosen expiration date, calculates the trading range, isolates at-the-money contracts, and loads results into PostgreSQL. Skills: OOP, SQLAlchemy, API integration, schema management Data source: Tradier Sandbox API

Salifort Motors - Employee Churn Prediction.ipynb — Logistic regression model forecasting employee attrition, with supporting EDA. Skills: data cleaning, EDA, Matplotlib/Seaborn, SciPy, scikit-learn, cross-validation Data source: HR Analytics Dataset (Kaggle)

Excel

Adidas US Sales EDA.xlsx — Analyzes operating margins and tests statistical significance across pivot table breakdowns. Skills: pivot tables/charts, slicers, hypothesis testing, formulas Data source: Adidas Sales Dataset (Kaggle)

2022 Milwaukee Property Sales Dashboard.xlsx — Dashboard analyzing residential property sales across Milwaukee. Skills: pivot tables/charts, slicers, XLOOKUP, filtering Data source: Milwaukee Open Data Portal

Tableau

Marketing Analysis: Term Deposit Campaign — Compares a current term deposit campaign to a prior one and identifies top-responding demographics. Data source: Moro, S., Rita, P., and Cortez, P. (2012). Bank Marketing. UCI Machine Learning Repository.

Adidas Dashboard — Tracks operating margin shifts by year, store location, and product category. Data source: Adidas Sales Dataset (Kaggle)

Known Limitations
Python pipeline depends on Tradier's Sandbox API, which uses delayed/sandbox data rather than live market feeds
Excel dashboards require manual refresh if underlying data is updated
Tableau dashboards are hosted on Tableau Public and require an internet connection to view
Important Notes
All datasets are either publicly available or generated via public sandbox APIs — see individual project sections for sources
SQL query outputs are saved in query results/ for quick reference without re-running the full analysis
