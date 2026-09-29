# Customer Shopping Behavior Analysis

## Overview

This project analyzes customer shopping behavior using **Python, Oracle SQL, and Power BI**.

The project follows an end-to-end data analytics workflow, starting with data loading and exploratory data analysis, followed by data cleaning, feature engineering, SQL-based business analysis, and Power BI visualization.

---

## Dataset

The dataset used in this project is:

`customer_shopping_behavior.csv`

The dataset contains **3,900 customer purchase records** with information related to:

- Customer demographics
- Products and categories
- Purchase amounts
- Locations
- Reviews
- Subscription status
- Shipping types
- Discounts
- Previous purchases
- Payment methods
- Purchase frequency

---

## Tools & Technologies

- **Python**
- **Pandas**
- **Jupyter Notebook**
- **Oracle Database**
- **Oracle SQL**
- **SQL Developer**
- **Power BI**
- **GitHub**

---

## Project Workflow

### 1. Data Loading

The customer shopping dataset was loaded into Python using Pandas.

```python
import pandas as pd

df = pd.read_csv("customer_shopping_behavior.csv")
```

The dataset was inspected using:

- `head()`
- `info()`
- `describe()`
- `isnull().sum()`

This helped understand the dataset structure, data types, statistical information, and missing values.

---

### 2. Exploratory Data Analysis

Exploratory Data Analysis (EDA) was performed to understand customer shopping behavior.

The analysis included:

- Dataset structure
- Customer demographics
- Purchase amounts
- Product categories
- Review ratings
- Subscription status
- Shipping types
- Discount usage
- Previous purchases
- Purchase frequency

---

### 3. Data Cleaning

The dataset was cleaned and standardized before performing SQL analysis.

The main cleaning steps included:

- Checking for missing values
- Handling missing review ratings
- Standardizing column names
- Renaming `purchase_amount_(usd)` to `purchase_amount`
- Checking redundant information
- Removing the redundant `promo_code_used` column

There were **37 missing values** in the Review Rating column.

The missing review ratings were filled using the median review rating within each product category.

---

### 4. Feature Engineering

Additional features were created to support the analysis.

#### Age Group

Customers were divided into four age groups:

- Young Adult
- Adult
- Middle-aged
- Senior

#### Purchase Frequency Days

Purchase frequency categories were converted into numerical day intervals.

| Purchase Frequency | Days |
|---|---:|
| Weekly | 7 |
| Fortnightly | 14 |
| Bi-Weekly | 14 |
| Monthly | 30 |
| Quarterly | 90 |
| Every 3 Months | 90 |
| Annually | 365 |

---

## Oracle Database Integration

After cleaning and transforming the dataset in Python, the data was loaded into an **Oracle Database**.

Python was connected to Oracle using:

- `oracledb`
- `SQLAlchemy`

The main table created in Oracle was:

`CUSTOMER`

The data was then verified and analyzed using Oracle SQL Developer.

---

## SQL Analysis

SQL queries were created to perform business-focused analysis on the customer data.

The analysis covers:

1. Repeat buyers by subscription status
2. Top 3 most purchased products in each category
3. Products with the highest discount percentage
4. Average spend and total revenue by subscription status
5. Average purchase amount by shipping type
6. Top 5 products based on average review rating
7. Customers who received discounts and spent more than the overall average
8. Total revenue by gender
9. Retrieving the first 20 customer records
10. Identifying the database owner/schema of the `CUSTOMER` table

### SQL Concepts Used

- `SELECT`
- `WHERE`
- `GROUP BY`
- `ORDER BY`
- Aggregate functions
- `CASE`
- Subqueries
- `ROW_NUMBER()`
- Window functions
- `FETCH FIRST`

The complete SQL queries are available in:

`customer_behaviour_analysis.sql`

---

## Power BI Dashboard

The cleaned customer data was used to create an interactive **Power BI dashboard**.

The dashboard focuses on customer shopping behavior and includes analysis related to:

- Customer demographics
- Purchase behavior
- Revenue
- Product categories
- Subscription status
- Discounts
- Shipping types
- Review ratings
- Customer purchasing patterns

The Power BI dashboard file is:

`customer_behaviour_dashboard.pbix`

---

## Project Report

A detailed project report was created to document the project workflow, methodology, analysis, and outcomes.

The report is available as:

`Customer_Shopping_Behavior_Analysis.pdf`

---

## Project Presentation

A PowerPoint presentation was created to present the project, analysis, and business insights.

The presentation file is:

`From-raw-transactions-to-business-decisions.pptx`

---

## Project Files

```text
Customer-Shopping-Behavior-Analysis/
│
├── Customer_Shopping_Behavior_Analysis.pdf
├── From-raw-transactions-to-business-decisions.pptx
├── README.md
├── customer_behaviour_analysis.ipynb
├── customer_behaviour_analysis.sql
├── customer_behaviour_dashboard.pbix
└── customer_shopping_behavior.csv
```

### File Description

| File | Description |
|---|---|
| `customer_shopping_behavior.csv` | Customer shopping dataset |
| `customer_behaviour_analysis.ipynb` | Jupyter Notebook containing Python analysis and outputs |
| `customer_behaviour_analysis.sql` | Oracle SQL queries used for business analysis |
| `customer_behaviour_dashboard.pbix` | Power BI interactive dashboard |
| `Customer_Shopping_Behavior_Analysis.pdf` | Detailed project report |
| `From-raw-transactions-to-business-decisions.pptx` | Project presentation |
| `README.md` | Project documentation |

---

## How to Run

### Python

Install the required libraries:

```bash
pip install pandas oracledb sqlalchemy
```

Open the Jupyter Notebook:

`customer_behaviour_analysis.ipynb`

Make sure `customer_shopping_behavior.csv` is available in the same folder.

Run the notebook cells sequentially to perform:

1. Data loading
2. Data inspection
3. Data cleaning
4. Exploratory Data Analysis
5. Feature engineering
6. Oracle database integration

---

### Oracle SQL

1. Open Oracle SQL Developer.
2. Connect to the Oracle Database.
3. Make sure the `CUSTOMER` table is available.
4. Open `customer_behaviour_analysis.sql`.
5. Execute the SQL queries to perform the business analysis.

---

### Power BI

1. Open `customer_behaviour_dashboard.pbix`.
2. Connect to the Oracle Database if required.
3. Refresh the data.
4. Use the dashboard visualizations and filters to explore customer shopping behavior.

---

## Skills Demonstrated

- Python
- Pandas
- Data Cleaning
- Exploratory Data Analysis
- Feature Engineering
- SQL
- Oracle SQL
- Oracle Database
- SQL Developer
- Database Integration
- Data Analysis
- Data Visualization
- Power BI
- Business Intelligence
- GitHub

---

## Conclusion

This project demonstrates an end-to-end data analytics workflow using **Python, Oracle SQL, and Power BI**.

The project transforms raw customer shopping data into a cleaned and structured dataset, performs exploratory analysis and SQL-based business analysis, and presents the analysis through an interactive Power BI dashboard.

It demonstrates how multiple data analytics tools can be used together to transform raw data into meaningful business analysis.
