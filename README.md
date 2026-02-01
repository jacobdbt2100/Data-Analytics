# Data Analytics

## 1. Introduction

**Data analysis** is a process of `modelling`, `analyzing`, and `interpreting` data to extract insights. A **Data Analyst** `collects`, `process`, and `analyze` data to identify trends/patterns and make informed decisions.

**Data mining:** The analytical process of applying statistical and machine-learning techniques to prepared data to uncover patterns, relationships, and predictive insights for decision-making.

**Data profiling:** The process of examining data structure, content, and quality to assess fitness for use and prevent issues in downstream analytics.

**Data validation:** The process of enforcing predefined rules and constraints to ensure data meets required standards as it flows through a pipeline.

Summarily, **data profiling** tells what the data looks like; **data validation** ensures the data meets what it should look like.

**Data lifecycle**: `Use case` > `Data collection` > `Storage` > `Processing` > `Analysis` > `Visualization` > `Reporting`

**Types of analytics**:

- **Descriptive:** `What happened?` e.g., A skincare brand sees 15,000 people clicked their Instagram ad last week, but only 500 purchased.
- **Diagnostic:** `Why did it happen?` e.g., Analysis shows that shipping costs made many customers abandon their carts at checkout.
- **Predictive:** `What will likely happen?` e.g., If nothing changes, the model forecasts cart drop-offs will keep increasing as shipping prices rise.
- **Prescriptive:** `What should we do?` e.g., The system recommends offering free shipping above $40 to increase checkout conversions.
- **Exploratory:** `What hidden opportunities exist?` e.g., Data reveals customers who buy face cleansers often buy serums within a week, suggesting a personalised follow-up email can boost revenue.

### 1.1 Data Sources
- Databases, spreadsheets, APIs, streaming data, SaaS applications (Salesforce, HubSpot, Shopify, etc.)
- Structured, Semi-structured, Unstructured data
- Data file formats: csv, xlsx, json, parquet
- Keys & relationships:
  - **Primary**: a unique identifier for each record in a table.
  - **Foreign keys**: a field in a table that refers to the primary key of another table, establishing a relationship between the two tables.
  - 1–1, 1–Many, Many–Many

### 1.2 Data Preparation (Cleaning & Transformation)

**Cleaning:**
- Duplicates
- Missing Values
- Data Types
- Data Formats
- Invalid Data
- Irrelevant Data
- Special Characters
- Outliers (statistical analysis)

**Transformation:**
- **Append:** combines data by adding rows. It stacks datasets with the same structure into one larger dataset, increasing the number of records without changing the columns.
- **Merge:** combines data by adding columns. It links datasets using a common field to bring related information from one dataset into another.
- Normalization vs Standardization (model building)

### 1.3 Exploratory Data Analysis (EDA)
- Descriptive statistics (mean, median, mode, std, percentiles)
- Distributions & variability
- Correlations
- Segmentation
  - `Demographic` (age, gender, income level, education, occupation, marital status)
  - `Geographic` (country, state, city, climate zones, urban vs rural, population density)
  - `Psychographic` (values & beliefs, interests/attitudes)
  - `Behavioural` (recency, frequency, monetary-RFM)

An unsupervised machine learning technique, `K-Means Clustering`, groups customers based on similarity in behaviour (advanced RFM analysis)
- Market basket analysis
- Cohort analysis

### 1.4 Business Understanding & Metrics
- KPIs
- Essential business metrics (marketing):
  - Engagement rate: measure/compare success of creating awareness about a product or service
  - Conversion rate: measure/compare sucess of users' completion of the desired business action (purchase, subscription)
  - Return on Ad Spend (ROAS)
  - Retention rate
 
### 1.5 Data Modelling Concepts
- `Schema:`a structured plan of how data is organized in a database. It defines:
  - `Tables (entities):` `Fact` vs `Dimension` tables
  - `Columns (attributes)`
  - `Data types:` integer, string, date, etc.
  - `Relationships:` between tables (primary keys, foreign keys)
  - `Constraints:` rules like NOT NULL, UNIQUE, etc.

- `Granularity:` level of detail stored in a dataset or table. `Higher granularity` means more detailed data (e.g., individual transactions). `Lower granularity` means summarized or aggregated data (e.g., monthly sales totals). Choosing the right granularity affects storage cost, query performance, and analytical usefulness.
  > `Example:`
    - Suppose you have a `Sales table`
      - `High granularity:` One row per item sold (e.g., “1 bottle of Coke sold at 10:05 AM”).
      - `Low granularity:` One row per day summarizing all items sold (e.g., “500 items sold on Monday”).
    - Choosing granularity depends on the analysis:
        - Analyse peak shopping hours > `High granularity`
        - Show monthly performance > `Low granularity`
  
- `Slowly Changing Dimensions (SCD):` describes attributes in a dimension table that change over time, but not frequently. `SCD techniques` ensure historical data remains accurate when those attributes change. There are different types (e.g., `Type 1:` overwrite old data; `Type 2:` add a new record to preserve history). SCDs are key to maintaining correct historical reporting and trend analysis.
  > `Example:`
        - A customer changes their `address` or `marital status`
        - Change in `cost` or `sales price`
- `Benefits of data modelling:`
  - `Data Quality:` ensures clean, structured, and consistent data
  - `Performance:` improves query speed
  - `Accuracy:` reduces duplication and errors
  - `Reusability:` reuse of data structures, definitions, and logic across multiple reports and systems

### 1.6 Data Visualisation & Insight Communication
- Chart selection best practices
- Storytelling with data
- Dashboards & Reports

### 1.7 Documentation
- Meta data
- Code, Queries (with comments)
- Version control basics (git)
- Communicating assumptions, limitations, and data decisions

### 1.8 Data Privacy and Security Concerns
- Data protection regulations
- Anonymizing sensitive data
- Secure data storage and transfer methods
- Access controls

## 2. Excel for Data Analysis

### 2.1 Excel Basics, Data Cleaning & Transformation

- Importing data (CSV, TXT, Excel files) 
- Data types, duplicates, missing values, invalid data, etc.
- **Text functions:** TRIM, CLEAN, LEFT, RIGHT, MID, FIND, LEN, TEXTSPLIT
- **Error handling:** IFERROR, ISBLANK, IFNA
- Combining text columns using CONCATENATE
- Data Validation (drop-down lists)
- Flash Fill for quick transformations
- Introduction to **`Power Query`** for automated data cleaning & transformation

### 2.2 Functions & Conditional Formatting

- **Math & Stats:** SUM, AVERAGE, MEDIAN, MODE, COUNT, MAX, MIN, STDEV, VAR
- **Logical:** IF, IFS, AND, OR
- **Conditional:** SUMIF, SUMIFS, AVERAGEIF, AVERAGEIFS, COUNTIFS
- **Lookup & Reference:** VLOOKUP, XLOOKUP, INDEX-MATCH
- **Dynamic Array Functions:** FILTER, SORT, UNIQUE, SEQUENCE
- **Conditional Formatting:** Highlight trends and outliers

### 2.3 Data Exploration

- **Pivot Tables & Charts**: a data summarization tool to aggregate and filter data in a spreadsheet. Key features:
  - `Grouping data`
  - `Filtering & Slicing`
  - `Sorting`
  - `Calculated fields:` for quick calculations—ratios, percentages, averages, sums, differences; directly within the pivot table.
  - `Visualization`
- **Descriptive Statistics** (with formulas & Data Analysis ToolPak)
- **Power Query:** combining multiple tables (merge & append)
- **Power Pivot:** to create relationships between multiple tables for advanced analysis. **`VLOOKUP`** or **`XLOOKUP`** become inefficient with large datasets.
- **DAX (Data Analysis Expressions):** enables more omplex, dynamic calculations across related tables than **`Calculated fields`** can handle.

### 2.4 Visualization & Dashboard Building

- Chart types and use cases:
  - Column, Bar, Line, Pie, Scatter, Histogram, Combo
- Dynamic charts with Excel Tables or named ranges
- Slicers and Timelines for interactive reports
- Dashboard design principles:
  - Layout consistency
  - Minimal colour palette
  - Clear KPI presentation
- Final **interactive dashboard** project

## 3. SQL

### 3.1 SQL Basics & Database Foundations

- **SQL definition** and how **databases** are structured

  **SQL (Structured Query Language)** is a standard programming language used to communicate with **`relational databases`** — systems that store data in tables (rows and columns). With SQL, you can:
  - Create databases and tables
  - Insert data into tables
  - Query data (ask questions to retrieve specific information)
  - Update existing data
  - Delete data
  - Control access (security)

  A **`database`** is an organized collection of data stored and accessed electronically. It provides a way to store, organize, and retrieve large amounts of data efficiently.

- **SQL Clauses**
  - `Query Logical Written Order:` `SELECT`, TOP, DISTINCT, `FROM`, `WHERE`, `GROUP BY`, HAVING, `ORDER BY`, LIMIT
  - `Query Logical Execution Order:`

| **Order** | **Clause**                       | **Purpose**                                    |
| --------- | -------------------------------- | -----------------------------------------------|
| 1️         | **FROM**                         | Identify the table(s) or source(s) of data.    |
| 2️         | **ON** *(if JOIN used)*          | Define join conditions between tables.         |
| 3️         | **JOIN**                         | Combine data from multiple tables.             |
| 4️         | **WHERE**                        | Filter rows before grouping.                   |
| 5️         | **GROUP BY**                     | Group rows that share the same values.         |
| 6️         | **HAVING**                       | Filter groups after aggregation.               |
| 7️         | **SELECT**                       | Choose which columns or expressions to return. |
| 8️         | **DISTINCT** *(if used)*         | Remove duplicate rows from the result.         |
| 9️         | **ORDER BY**                     | Sort the final results.                        |
| 10        | **TOP / LIMIT / OFFSET / FETCH** | Restrict the number of rows returned.          |

- Filtering with `logical operators` (AND, OR, NOT, BETWEEN, IN, LIKE)
- Aliases for `columns` and `tables` (especially with joins)
  - `ALIAS command` in SQL is the name that can be given to any table or a column.

**Example Queries:**
```sql
-- Create a simple table
CREATE TABLE customers (
    customer_id SERIAL PRIMARY KEY,
    name VARCHAR(50),
    country VARCHAR(50),
    age INT
);

-- Insert sample data
INSERT INTO customers (name, country, age)
VALUES

('John Doe', 'Nigeria', 30),
('Mary Smith', 'Kenya', 25),
('Adewale Ogun', 'Nigeria', 41);

-- Retrieve and filter
SELECT name, country, age
FROM customers
WHERE country = 'Nigeria'
ORDER BY age DESC;
```

### 3.2 Data Aggregation

- Aggregate Functions: COUNT, SUM, AVG, MIN, MAX
- GROUP BY and HAVING
- DISTINCT and aggregate filtering
- Derived columns using CASE

**Example Queries:**

```sql
-- Count customers by country
SELECT country, COUNT(*) AS total_customers
FROM customers
GROUP BY country;

-- Average age of customers per country (filter countries with more than 1)
SELECT country, ROUND(AVG(age), 1) AS avg_age
FROM customers
GROUP BY country
HAVING COUNT(*) > 1;

-- Conditional logic with CASE
SELECT 
    name,
    age,
    CASE 
        WHEN age < 30 THEN 'Young'
        WHEN age BETWEEN 30 AND 45 THEN 'Mid Age'
        ELSE 'Senior'
    END AS age_group
FROM customers;
```

### 3.3 Data Cleaning, Joins & CTEs

- Data cleaning with TRIM, LOWER, UPPER, REPLACE
- Handling NULLs with COALESCE, IS NULL, IS NOT NULL
- JOINS in SQL
  
  A `join` is an operation used to combine rows from two or more tables based on related columns. It enables data retrieval from multiple tables simultaneously. Types: `INNER JOIN`, `LEFT JOIN`, `RIGHT JOIN`, `FULL JOIN`, `CROSS JOIN`, `SELF JOIN`.

- Subqueries and CTEs (Common Table Expressions)
  - A `subquery` is a query nested inside another query. A `correlated subquery` is a subquery that depends on the outer query. It runs once for each row returned by the outer query.
  - A `CTE` (Common Table Expression) is a temporary named result set that can be referenced within a SQL query. It makes complex queries easier to read and manage — especially when using subqueries or recursion. A `recursive CTE` is a CTE that refers to itself to handle hierarchical or sequential data, such as organization charts, family trees, or folder structures.

**Example Queries:**

```sql
-- Create an orders table
CREATE TABLE orders (
    order_id SERIAL PRIMARY KEY,
    customer_id INT,
    amount DECIMAL(10,2),
    order_date DATE
);

-- Join customers and orders
SELECT 
    c.name,
    o.order_id,
    o.amount,
    o.order_date
FROM customers AS c
LEFT JOIN orders AS o
ON c.customer_id = o.customer_id;

-- Use CTE to find top spenders
WITH total_spent AS (
    SELECT customer_id, SUM(amount) AS total_amount
    FROM orders
    GROUP BY customer_id
)
SELECT c.name, t.total_amount
FROM customers AS c
JOIN total_spent AS t
ON c.customer_id = t.customer_id
ORDER BY t.total_amount DESC;
```

### 3.4 Query Optimization & Final Project

- Query performance techniques (basics)
  - LIMIT
  - Indexes
  - Avoiding SELECT *
  - Partitioning

- Joins with filters and aggregation
- Window functions (ROW_NUMBER, RANK, SUM OVER)
- Mini analytical **case studies** project

**Example Queries:**

```sql
-- Using a window function to rank customers by total order amount
SELECT 
    c.name,
    SUM(o.amount) AS total_spent,
    RANK() OVER (ORDER BY SUM(o.amount) DESC) AS spending_rank
FROM customers c
JOIN orders o ON c.customer_id = o.customer_id
GROUP BY c.name;

-- Simple data quality check
SELECT *
FROM orders
WHERE amount IS NULL OR amount <= 0;

-- Top 3 customers per country by total spending
WITH country_rank AS (
    SELECT 
        c.country,
        c.name,
        SUM(o.amount) AS total_spent,
        ROW_NUMBER() OVER (PARTITION BY c.country ORDER BY SUM(o.amount) DESC) AS rnk
    FROM customers c
    JOIN orders o ON c.customer_id = o.customer_id
    GROUP BY c.country, c.name
)
SELECT * 
FROM country_rank
WHERE rnk <= 3;
```

### MISCELLANEOUS

#### `DELETE vs TRUNCATE:`
`DELETE` removes specific rows from a table using a condition. `TRUNCATE` removes all rows from a table.

#### `UNION vs UNION ALL:`
`UNION` and `UNION ALL` are used to combine the result sets of two or more SELECT statements. `UNION` removes duplicate rows from the combined result set. `UNION ALL` includes all rows, including duplicates.

#### `Transaction:`
A `transaction` is a sequence of SQL statements that are executed as a single logical unit of work. It ensures data consistency and integrity by either committing all changes or rolling them back if an error occurs.

#### `Clustered vs Non-clustered Index:`
A `clustered Index` determines the physical order of data in a table. It changes the way the data is stored on disk and can be created on only one column. A table can have only one clustered index.

A `Non-clustered Index` does not affect the physical order of data in a table. It is stored separately and contains a pointer to the actual data. A table can have multiple non-clustered indexes.

#### `ACID in database transactions:`
`ACID` stands for Atomicity, Consistency, Isolation,and Durability. It is a set of properties that guarantee reliable processing of database transactions.
  - `Atomicity` ensures that a transaction is treated as a single unit of work, either all or none of the changes are applied.
  - `Consistency` ensures that a transaction brings the database from one valid state to another
  - `Isolation` ensures that concurrent transactions do not interfere with each other
  - `Durability` ensures that once a transaction is committed, its changes are permanent and survive system failures.

#### `Database vs Schema:`

| **Aspect**     | **Database**                                                                    | **Schema**                                                                                            |
| -------------- | ------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------------- |
| **Definition** | A container for all data and objects such as **tables, views, and procedures**. | A container within a database that holds objects like **tables and views**, defining their ownership. |
| **Hierarchy**  | Higher level — contains schemas.                                                | Lower level — exists inside a database.                                                               |

`Why schemas are useful:`

  - They help organise database objects (e.g. separating sales and HR tables).
  - They control access — permissions can be granted per schema.
  - They prevent naming conflicts between objects.

#### `Temporary table vs Table variable:`

| **Aspect**     | **Temporary Table**                         | **Table Variable**                             |
| -------------- | ------------------------------------------- | ---------------------------------------------- |
| **Definition** | A table stored temporarily in the database. | A variable that holds table data in memory.    |
| **Scope**      | Exists for a session or transaction.        | Exists within a batch, procedure, or function. |
| **Storage**    | Stored in tempdb.                           | Primarily stored in memory.                    |
| **Lifetime**   | Dropped when session or transaction ends.   | Deallocated when its scope ends.               |

#### `Stored Procedure:`
Is a saved set of SQL commands that performs a specific task — like retrieving, inserting, updating, or deleting data — and can be executed repeatedly. Can be with or without `parameters`.

#### `View:`
A `view` is a virtual table based on the result of an SQLstatement. A `materialized view` is a physical copy of the view's result set stored in the database, which is updated periodically.

#### `IN vs EXISTS:`

| **Aspect**       | **IN**                                                                                    | **EXISTS**                                                                            |
| ---------------- | ----------------------------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| **Purpose**      | Checks if a value exists **within a list or subquery result**.                            | Checks if **any row** exists in a subquery that meets the condition.                  |
| **How it works** | Compares values directly.                                                                 | Tests for the **existence** of rows — stops checking once it finds one match.         |                       
#### `Data Warehouse:`
Is a large, centralized repository that stores and manages data from various sources designed for efficient analysis and reporting purposes.

#### `Primary key vs Candidate key:`
A `primary key` is a chosen candidate key that uniquely identifies a row in a table. A `candidate key` is a set of one or more columns that could potentially become the primary key.

#### `GRANT:`
The `GRANT statement` is used to grant specific permissions or privileges to users or roles in a database.

#### `COALESCE:`
The `COALESCE function` returns the first non-null expression from a list of expressions. It is often used to handle null values effectively.

#### `ROW_NUMBER():`
The `ROW_NUMBER() function` assigns a unique incremental number to each row in the result set.

#### `Some Purposes of SQL Functions:`
- Perform some calculations on the data
- Modify individual data items
- Manipulate output
- Format dates and numbers
- Convert data types

#### `SQL Commands:`
`SQL commands` are grouped based on what they do in a database. Here’s a simple breakdown:

1. **DDL (Data Definition Language):** `define`, `alter`, or `remove` database structures.

| **Command** | **Purpose**                                                |
| ----------- | ---------------------------------------------------------- |
| `CREATE`    | Creates a new database object (table, view, schema, etc.). |
| `ALTER`     | Modifies an existing object.                               |
| `DROP`      | Deletes an object permanently.                             |
| `TRUNCATE`  | Removes all data but keeps the table structure.            |
| `RENAME`    | Changes the name of a database object.                     |

2. **DML (Data Manipulation Language):** `manipulate data` stored in tables.

| **Command** | **Purpose**                                                                    |
| ----------- | ------------------------------------------------------------------------------ |
| `INSERT`    | Adds new records.                                                              |
| `UPDATE`    | Modifies existing records.                                                     |
| `DELETE`    | Removes specific records.                                                      |
| `MERGE`     | Combines `INSERT`, `UPDATE`, and `DELETE` in one statement (used for upserts). |

`MERGE` adds new rows or updates existing ones in a single step (used when matching data from two tables).

3. **DCL (Data Control Language):** `control` access and privileges.

| **Command** | **Purpose**               |
| ----------- | ------------------------- |
| `GRANT`     | Gives user permissions.   |
| `REVOKE`    | Removes user permissions. |

4. **TCL (Transaction Control Language):** `manage transactions` and maintain data integrity.

| **Command** | **Purpose**                                        |
| ----------- | -------------------------------------------------- |
| `COMMIT`    | Saves changes made in a transaction.               |
| `ROLLBACK`  | Reverses changes before commit.                    |
| `SAVEPOINT` | Sets a point to roll back to within a transaction. |

5. **DQL (Data Query Language):** `query` and retrieve data.

| **Command** | **Purpose**                             |
| ----------- | --------------------------------------- |
| `SELECT`    | Retrieves data from one or more tables. |

#### `SQL Commands & Functions Overview:`

| **Category**                     | **Key Commands / Functions**                                                                                       | **Notes & Use Cases**                                          |
| -------------------------------- | ------------------------------------------------------------------------------------------------------------------ | -------------------------------------------------------------- |
| **Basics**                    | `SELECT`, `FROM`, `WHERE`, `GROUP BY`, `HAVING`, `ORDER BY`, `LIMIT` / `TOP`, `DISTINCT`                              | Foundation of all SQL queries.                                 |
| **Operators**                 | `=`, `!=`, `<`, `>`, `<=`, `>=`, `BETWEEN`, `IN`, `NOT IN`, `LIKE`, `ILIKE`, `AND`, `OR`, `NOT`                       | Used to filter and compare values.                             |
| **Aggregate Functions**       | `COUNT()`, `SUM()`, `AVG()`, `MIN()`, `MAX()`, `MEDIAN()`, `MODE()`, `STDDEV()`                                       | Summarise or aggregate data — often used with `GROUP BY`.      |
| **String Functions**          | `CONCAT()`, `REPLACE()`, `UPPER()`, `LOWER()`, `LTRIM()`, `RTRIM()`, `TRIM()`, `SUBSTRING()`, `LEN()` / `LENGTH()`    | Used for text manipulation and cleaning.                       |
| **Date & Time Functions**     | `GETDATE()`, `CURRENT_DATE`, `YEAR()`, `MONTH()`, `DAY()`, `DATEDIFF()`, `DATEADD()`, `DATE_TRUNC()`, `DATE_FORMAT()` | Handle and format date/time values.                            |
| **Cleaning & Transformation** | `CAST()`, `CONVERT()`, `COALESCE()`, `NULLIF()`, `CASE WHEN`, `IFNULL()`, `IIF()`, `LISTAGG()`                        | Data formatting, null handling, and conditional logic.         |
| **Set Operations**            | `UNION`, `UNION ALL`, `INTERSECT`, `EXCEPT` / `MINUS`                                                                 | Combine or compare results from multiple queries.              |
| **Window Functions**          | `ROW_NUMBER()`, `RANK()`, `DENSE_RANK()`, `LEAD()`, `LAG()`, `SUM() OVER(...)`, `AVG() OVER(...)`                     | Perform calculations across rows without grouping.             |

#### `RANK() vs DENSE_RANK():`

| **Function**       | **Description**                                  | **Example (Scores: 95, 90, 90, 85)**                             | **Resulting Ranks** |
| ------------------ | ------------------------------------------------ | ---------------------------------------------------------------- | ------------------- |
| **`RANK()`**       | Assigns ranks with gaps when there are ties.     | Two people tied at 90 both get rank 2; the next rank skips to 4. | 1, 2, 2, **4**      |
| **`DENSE_RANK()`** | Assigns consecutive ranks without gaps for ties. | Two people tied at 90 both get rank 2; the next rank is 3.       | 1, 2, 2, **3**      |

## 4. Power BI

### 4.1 Power BI Basics

**Data visualization:** the practice of presenting data in graphical or pictorial formats—such as charts, graphs, maps, and dashboards—to clearly communicate patterns, trends, and insights.

**Power BI:** is a business intelligence tool developed by Microsoft that allows users to connect, transform, analyze, and visualize data from multiple sources.

- `Power BI` main Components:
  - `Desktop:` Windows application for building reports and data models.
  - `Service (Power BI Online):` cloud-based platform for publishing, sharing, and collaborating on reports and dashboards.
  - `Mobile:` mobile apps for viewing and interacting with reports on phones and tablets.
  - `Gateway:` a bridge that connects on-premises data sources to Power BI Service for scheduled refreshes.
  - `Report Server:` on-premises server for hosting and managing Power BI reports within an organization’s own infrastructure.
  - `Embedded:` a service for developers to embed Power BI reports and dashboards into custom applications.
  - `Power Query:` data connection and transformation engine used across Power BI for data cleaning and preparation.
  - `Power Pivot:` data modelling engine that allows creating relationships, measures, and calculated columns using DAX.

- Power BI Desktop, with three main views (or panes), each serving a different purpose:
  - `Report View:` build and design dashboards using visuals, charts, and slicers.
  - `Data View:` see and explore loaded tables after data has been imported.
  - `Model View:` define relationships between tables.

- Data import from Excel, CSV, and SQL databases
- Understanding Power Query Editor
- Data profiling (column quality, distribution, profile)
- Cleaning and transforming data:
  - Remove duplicates, split columns, replace values, fill blanks
  - Merge and append queries
- Basic data model setup (naming conventions, data types, relationships)

### 4.2 Data Modelling & DAX Fundamentals

- Star schema design: fact and dimension tables
- Relationships (one-to-many, cross filter direction)
- Calculated columns vs. measures
- DAX basics:
  - SUM, AVERAGE, COUNTROWS, DISTINCTCOUNT, CALCULATE, FILTER, ALL
- Conditional logic: IF, SWITCH
- Time intelligence:
  - TOTALYTD, SAMEPERIODLASTYEAR, DATEADD

### 4.3 Data Visualisation & Interactivity

- Chart types and when to use them:
  - Bar/Column, Line, Card, Pie, Map, Matrix
- Hierarchies (e.g., Year > Quarter > Month)
- Slicers, Filters, and Drill-throughs
- Conditional formatting and custom tooltips
- Using bookmarks for dynamic storytelling

### 4.4 Dashboard Design, Publishing & Storytelling

- Dashboard layout and design principles:
  - Consistent alignment, colours, and typography
- Clear KPIs at the top, supporting visuals below
- Storytelling techniques for business insights
- Using Power BI Service:
- Publishing reports
- Creating and managing workspaces
- Sharing dashboards and setting permissions
- Report refresh and basic automation
- Export options (PDF, PowerPoint, shared link)
- Final **interactive dashboard** project

## 5. Python for Data Analysis





