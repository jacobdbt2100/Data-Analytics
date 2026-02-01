# Data Analytics

## 1. Foundations of Data Analysis

**Data analysis** is a process of `modelling`, `analyzing`, and `interpreting` data to extract insights. A **Data Analyst** `collects`, `process`, and `analyze` data to identify trends/patterns and make informed decisions.

**Data lifecycle**: `Use case` > `Data collection` > `Storage` > `Processing` > `Analysis` > `Visualization` > `Reporting`

**Types of analytics**:

- **Descriptive:** What happened? e.g., A skincare brand sees 15,000 people clicked their Instagram ad last week, but only 500 purchased.
- **Diagnostic:** Why did it happen? e.g., Analysis shows that shipping costs made many customers abandon their carts at checkout.
- **Predictive:** What will likely happen?e.g., If nothing changes, the model forecasts cart drop-offs will keep increasing as shipping prices rise.
- **Prescriptive:** What should we do? e.g., The system recommends offering free shipping above $40 to increase checkout conversions.
- **Exploratory:** What hidden opportunities exist? e.g., Data reveals customers who buy face cleansers often buy serums within a week, suggesting a personalised follow-up email can boost revenue.

## 2. Data Sources
- Databases, spreadsheets, APIs, streaming data, SaaS applications (Salesforce, HubSpot, Shopify, etc.)
- Structured, Semi-structured, Unstructured data
- Data file formats: csv, xlsx, json, parquet
- Keys & relationships:
  - **Primary**: a unique identifier for each record in a table.
  - **Foreign keys**: a field in a table that refers to the primary key of another table, establishing a relationship between the two tables.
  - 1–1, 1–Many, Many–Many

## 3. Data Preparation (Cleaning & Transformation)
- Duplicates
- Missing Values
- Data Types
- Data Formats
- Invalid Data
- Irrelevant Data
- Special Characters
- Outliers (statistical analysis)
- Normalization vs Standardization (model building)

## 4. Exploratory Data Analysis (EDA)
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

## 5. Business Understanding & Metrics
- KPIs
- Essential business metrics (marketing):
  - Engagement rate: measure/compare success of creating awareness about a product or service
  - Conversion rate: measure/compare sucess of users' completion of the desired business action (purchase, subscription)
  - Return on Ad Spend (ROAS)
  - Retention rate
 
## 6. Data Modelling Concepts
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

## 7. Data Visualisation & Insight Communication
- Chart selection best practices
- Storytelling with data
- Dashboards & Reports

## 8. Documentation
- Meta data
- Code, Queries (with comments)
- Version control basics (git)
- Communicating assumptions, limitations, and data decisions

### MISCELLANEOUS

#### `Data Analysis vs Data Analytics:`

| Aspect                | **Data Analysis**                                                                                      | **Data Analytics**                                                                       |
| --------------------- | ------------------------------------------------------------------------------------------------------ | ---------------------------------------------------------------------------------------- |
| **Definition**        | The process of modelling, analyzing, and interpreting data to extract insights. | A broader discipline that includes data collection, data engineering, data science, data analysis, and insight delivery to support decision-making. |
| **Scope**             | Narrower — focused on answering specific questions.                         | Broader — covers full data lifecycle: Data collection > Storage > Processing > Analysis > Visualization > Communication.                                   |

Summarily, **`Data Analysis`** is a `task` — extracting insights from data. **`Data Analytics`** is a field — encompassing the processes that make insights possible.

#### `Data Mining vs Data Profiling:`

| Aspect            | **Data Mining**                                                     | **Data Profiling**                                              |
| ----------------- | ------------------------------------------------------------------- | --------------------------------------------------------------- |
| **Purpose**       | Extract hidden patterns, correlations, and insights from data       | Understand data quality, structure, and anomalies               |
| **Focus**         | Analytics, prediction, and decision support                         | Assessing data fitness for use before analytics                 |
| **Techniques**    | Machine learning, statistical modelling, clustering, classification | Completeness checks, data type validation, frequency analysis   |
| **Output**        | Trends, predictive models, actionable insights                      | Data quality metrics, metadata summaries                        |
| **Project Stage** | Typically after data preparation                                    | Early phase of data pipeline (before cleansing/transformation)  |
| **Key Benefit**   | Drives strategic and operational decisions                          | Reduces errors and improves reliability of downstream analytics |

#### `Data Normalization:`
The process of structuring data to reduce redundancy and improve integrity—typically by organizing it into related tables and enforcing rules (normal forms) so that each data point is stored once and updated consistently.

#### `Data Warehouse:`
A large centralized repository of data used for reporting and analysis, combining and organizing data from different sources for efficient querying and reporting.

#### `Handling Large Datasets:`
Requires the use of efficient data storage and processing techniques such as;
- SQL databases
- Parallel computing: running multiple computations at the same time across multiple processors, rather than sequentially on a single one.
- Cloud-based solutions
- Code optimization (performance tuning)

#### `Data Privacy and Security Concerns:`
- Data protection regulations
- Anonymizing sensitive data
- Secure data storage and transfer methods
- Access controls
