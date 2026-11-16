### UNIT III – DATA WAREHOUSING & OLAP

I've referred to your uploaded 3-page Unit III material. These notes cover all 5 topics in your syllabus, with simple explanations, diagrams, examples, comparison tables, and important exam points.

I'll keep them moderately detailed so you can understand and write them in an 8-mark answer without having to memorize lengthy paragraphs.

### 1\. Data Warehouse and Its Architecture

### Definition

A Data Warehouse is a centralized repository used to store large amounts of data collected from multiple sources for reporting, analysis, and decision-making.

It stores integrated historical data and helps organizations identify trends and make better decisions.

### Characteristics of Data Warehouse

Remember the mnemonic SITN.

* Subject-Oriented: Data is organized around subjects such as sales, customers, and products.

* Integrated: Data is collected from different sources and stored in a consistent format.

* Time-Variant: Stores historical data over a long period to analyze changes and trends.

* Non-Volatile: Stored data is stable and is not frequently changed or deleted.

### Three-Tier Architecture of Data Warehouse

A Data Warehouse architecture consists of three major layers.

![Medium](https://images.openai.com/static-rsc-4/YizbgGHi_MOMItt81GyROLWFhgVa7cMXFIuUDDqSPMLvO80Klms7ti_qcKkY4YqQuw3tiIWpLzGPPneYZe-ou6alosjJA9sISpb-YztIpF-LmbeQERAlH0EHFQha23MLl_HfxdABG2SKRP14Jb2mmk22MExyXqy3ProscW5iTdjsM0zDr34AcWqnIVmyx7nk?purpose=fullsize)

### 1\. Bottom Tier – Data Sources

* Contains data collected from different sources.

* Sources include operational databases, external sources, legacy systems, social media, and sensors.

* Data is extracted, transformed, and loaded using the ETL process.

Example: Sales database, Excel files, websites, and customer records.

### 2\. Middle Tier – Data Warehouse and OLAP Server

* Stores integrated and historical data in the data warehouse.

* The OLAP server helps perform multidimensional data analysis.

* Provides processed data to the upper layer.

Example: An organization storing five years of sales data for analysis.

### 3\. Top Tier – Front-End Tools

* Provides an interface for users to access and analyze data.

* Includes query tools, reports, OLAP analysis, and data mining.

* Helps users understand information and make decisions.

Example: A manager viewing monthly sales reports and graphs.

### ETL Process

ETL stands for:

* E – Extract: Collect data from different sources.

* T – Transform: Clean and convert data into a common format.

* L – Load: Store the processed data in the data warehouse.

![ETL vs ELT: Which One Should You Use and Why? - DEV Community](https://images.openai.com/static-rsc-4/XdZrRrG2_y8PICWLuBsLD9g37R0cwyT9cUANA2A6FKbQFj-761y-sUMBqG7obDkSLdwJLnCisDRQfxn5OHRcUeJcyc9McZl9Xuj9qBzClRH6OpizuwP2LApKc7Q_uTgPFXtOzuEg3xYTUE2TzKoDYkAbI1UGwvzBzo0KCxBxjz6r4eCmNoUM0467J13Hme58?purpose=fullsize)

### Real-World Example

Consider an online shopping company:

* Customer details are collected from databases.

* Product and sales information is collected from different systems.

* All information is integrated and stored in a data warehouse.

* Managers use reports to identify popular products and monthly sales trends.

### Advantages

* Stores large amounts of historical data.

* Combines data from multiple sources.

* Supports better decision-making.

* Helps identify trends and patterns.

* Makes reporting and analysis easier.

Conclusion: A data warehouse provides a centralized location for storing integrated historical data and supports efficient analysis and decision-making.

Reference: Uploaded Unit III notes, page 1.

### 2\. Star Schema, Snowflake Schema and Fact Constellation

### Definition

A Schema is the logical structure that describes how data is organized in a data warehouse, including fact tables and dimension tables.

There are three important types of schemas.

### A. Star Schema

### Definition

Star Schema is a data warehouse schema in which one central fact table is connected to multiple dimension tables, forming a star-like structure.

### Components

* Fact Table: Stores measurable data such as sales amount and quantity sold.

* Dimension Tables: Store descriptive information such as time, location, and product.

### Diagram

![Understanding Star Schema in Data Warehouse Modelling](https://images.openai.com/static-rsc-4/yWx3QKb0LbMW0Nwd3j_uhL0QITuc7gVhAq4gX0RMx-bVZMOAamlpzJ5QzQMkimEaRdlGRe8oSrc5dFNduhlwsyzBMB0dN1BeUazyBJgxatwr1VZHu7y83W-YuwTszfMm66Yrg1-B0gCm2ZDE3JbDxPSnMv-Z3tRfFBApI9LDCvpc-TmqqGPkLVLKh5-u1T6k?purpose=fullsize)

### Example

A supermarket sales database:

* Fact Table: Sales amount, quantity sold.

* Time Dimension: Day, month, year.

* Product Dimension: Product name, category.

* Location Dimension: City, state, country.

Key Point: Simple structure and faster queries, but more data redundancy.

### B. Snowflake Schema

### Definition

Snowflake Schema is a variation of the Star Schema in which dimension tables are normalized and divided into smaller related tables.

### Diagram

![Data Warehouses and OLAP — Slides for Textbook — — Chapter 2 — -  ppt download](https://images.openai.com/static-rsc-4/Ada63Ui9SV9Sm8IsNUumpGYAEmGAAfBUmXeCIYlwKErV_rXPeXhfxVEBkZdOEwK4eOrS1ZbbiVNQtsP_136jnzsjPcFFZG0BR38urLa6H622FTV3YOC08d6lUljS4fBfF10ULSp42yeD2xfIJ2uMwVb9-F9jiNuf-uCDlrtTL9IF2Q6RaDsfWwQDqz8fQ1vL?purpose=fullsize)

### Example

In a Star Schema, the Location table may contain:

| City      | State      | Country |
| --------- | ---------- | ------- |
| Hyderabad | Telangana  | India   |
| Chennai   | Tamil Nadu | India   |

In a Snowflake Schema, these details are separated:

* City Table

* State Table

* Country Table

Key Point: Reduces redundancy and storage but increases query complexity.

### C. Fact Constellation (Galaxy Schema)

### Definition

Fact Constellation is a schema containing multiple fact tables that share common dimension tables. It is considered a collection of star schemas.

### Diagram

![PPT - Principles of Data Warehousing PowerPoint Presentation, free download - ID:1658424](https://images.openai.com/static-rsc-4/Btpc1tKS7JX9mxaPGryLCr3kwNltcL93IomXT_rj5z_xw5peUO7LgbOrnYtdvKWZjfVOk11YXxecA18MXWwRgNljUZkLAzYYC4Aq0o98jO9RN2OmBL4A53zzHSGbDQQmX5dLPCsuFNZRU0Gv6VU8zaBvuuoi0VhgLmFjZjw-VgpiM7R1UZDczsu3OMjUAVDg?purpose=fullsize)

### Example

An online shopping company has:

* Sales Fact Table

* Shipping Fact Table

Both tables share common dimensions such as Time and Location.

Key Point: Suitable for large organizations requiring analysis of multiple business processes.

### Comparison of Star, Snowflake and Fact Constellation

| Feature          | Star            | Snowflake           | Fact Constellation       |
| ---------------- | --------------- | ------------------- | ------------------------ |
| Fact Tables      | One             | One                 | Multiple                 |
| Dimension Tables | Denormalized    | Normalized          | Shared                   |
| Complexity       | Simple          | Moderate            | Complex                  |
| Query Speed      | Fastest         | Slower              | Moderate                 |
| Redundancy       | High            | Low                 | Low                      |
| Storage          | More            | Less                | Less                     |
| Used For         | Simple analysis | Complex hierarchies | Enterprise-wide analysis |

### Easy Way to Remember

* Star: One fact table + simple dimensions.

* Snowflake: One fact table + split dimensions.

* Galaxy: Multiple fact tables + shared dimensions.

Reference: Uploaded Unit III notes, pages 1–2.

### 3\. OLAP Operations

### Definition

OLAP (Online Analytical Processing) operations are used to analyze multidimensional data stored in a data cube from different perspectives.

They help users summarize data, view detailed information, and compare data across different dimensions.

### What is a Data Cube?

A Data Cube is a multidimensional representation of data used for analysis.

It organizes information based on dimensions such as:

* Time: Day, Month, Year.

* Location: City, State, Country.

* Product: Mobile, Laptop, Tablet.

![MultiDimensional Data Model - GeeksforGeeks](https://images.openai.com/static-rsc-4/U05J7r6LtsBbomazgx1Ed2S1tZMOmu1piEVmubO-FFs0MOFpYhsBYuw3DaDBa7GgRuQgBxz7AUT73bzJHAPZX82xdG_a_Vv-hISxqwIwu99vYbNWJgcwnZmcAt8aNyul8SfJ39nbqpslg6Min16YVN0M65j7fFjFMLBjzpl_0bbCeC7nCD_hnIdPACkQGtHi?purpose=fullsize)

### Five Important OLAP Operations

Remember: R-D-S-D-P

### 1\. Roll-Up (Drill-Up)

* Summarizes data by moving from a lower level to a higher level in a concept hierarchy.

* Reduces the level of detail.

Example:

```text
City → State → Country

Hyderabad ─┐
Chennai   ─┼──→ India (Total Sales)
Mumbai    ─┘
```

Daily sales → Monthly sales → Yearly sales.

### 2\. Drill-Down (Roll-Down)

* Opposite of Roll-Up.

* Moves from summarized data to more detailed data.

Example:

```text
Yearly Sales
      |
Quarterly Sales
      |
 Monthly Sales
      |
  Daily Sales
```

### 3\. Slice

* Selects only one particular value from one dimension.

* Produces a smaller sub-cube.

Example:

Selecting only `Time = Q1` to view sales during the first quarter.

![OLAP Operations in Data Mining - Scaler Topics](https://images.openai.com/static-rsc-4/ogshuzz1gd8l636zTT5sew7fq7sbMnlfAATog3NpP-J3pjhXn5jn8NfgRNiOrKQE25Rl5DVK4h6gVHoCzNuf9IiZdT6g9uKB3ot-ChszsQe40jQkR7o25r72VcWjvROSzyYuL_LLy1L2wM71sqdkEL-pRmUlTCFat_17-nUEnb6YfkITv3RihWniEoTLfxLk?purpose=fullsize)

### 4\. Dice

* Selects a range of values from multiple dimensions.

* Produces a smaller sub-cube.

Example:

Selecting:

* Location = Hyderabad and Chennai.

* Time = Q1 and Q2.

* Item = Mobile and Laptop.

![Data Warehouse System](https://images.openai.com/static-rsc-4/rcyUKhMnPOpvAOTquZmes37MKxkeSOSbCT2eULaeSz7Dg8EhXb_0bUaoFSKArL89KujpxnOuXJOZ8bR2zciotH-HQebFEzk-nY7O8_Pf9Dx9pxchREbMkAvjbgXibStwVfqZSkHf8x2UBKlpE6J9jicFmY5K97CrycHXPbbZXwd4hbo44Lhc86nKwJDaOh0h?purpose=fullsize)

### 5\. Pivot (Rotate)

* Rotates the data cube to provide a different view.

* Changes the orientation of dimensions by swapping rows and columns.

Example:

Before Pivot:

| Time | Hyderabad | Chennai |
| ---- | --------- | ------- |
| Q1   | 500       | 400     |
| Q2   | 600       | 450     |

After Pivot:

| Location  | Q1  | Q2  |
| --------- | --- | --- |
| Hyderabad | 500 | 600 |
| Chennai   | 400 | 450 |

![OLAP | PPTX](https://images.openai.com/static-rsc-4/onqA0UYf5kzC-1jeiKL6GmXUHbItNMSotUYO2mDw_sWHnmpf28D9K9OLWZDgyV8EVXOgGpAtCzYnAK4KvOhDvL1iREU4e70WQnku_XSwxh4sakpWDd0LUBubfeLrV3X867V-ASzIBvQA22clnFkOL3qaOW_wI1OY13Q-0EjBlYKO58MF0_zJxwS6I_YY0b_q?purpose=fullsize)

### Comparison of OLAP Operations

| Operation  | Main Purpose              | Example                      |
| ---------- | ------------------------- | ---------------------------- |
| Roll-Up    | Summarizes data           | City → Country               |
| Drill-Down | Shows more detail         | Year → Month                 |
| Slice      | Fixes one dimension       | Time = Q1                    |
| Dice       | Fixes multiple dimensions | Q1 + Q2, Hyderabad + Chennai |
| Pivot      | Changes data view         | Swapping rows and columns    |

### Memory Trick

RDSDP

* R – Roll-Up

* D – Drill-Down

* S – Slice

* D – Dice

* P – Pivot

Conclusion: OLAP operations help users analyze multidimensional data from different perspectives and support better decision-making.

Reference: Uploaded Unit III notes, page 2.

### 4\. OLAP Servers

### Definition

OLAP Servers are systems that sit between the data warehouse and front-end tools and perform multidimensional data analysis.

They help users analyze large amounts of data quickly and efficiently.

### Types of OLAP Servers

There are three major types:

### 1\. ROLAP (Relational OLAP)

Definition: ROLAP uses relational databases (RDBMS) to store and analyze data using SQL queries.

Working:

* Stores data in relational tables.

* Uses SQL queries to retrieve information.

* Performs aggregation and analysis when queries are executed.

Example: MicroStrategy, SAP BW.

Best For: Very large datasets.

### 2\. MOLAP (Multidimensional OLAP)

Definition: MOLAP uses multidimensional data cubes with precomputed summaries for fast analysis.

Working:

* Stores data in multidimensional cubes.

* Precalculates summaries and aggregations.

* Provides very fast query responses.

Example: IBM Cognos PowerPlay, Oracle Essbase.

Best For: Fast query response and moderate data size.

### 3\. HOLAP (Hybrid OLAP)

Definition: HOLAP combines the features of ROLAP and MOLAP.

Working:

* Detailed data is stored in relational databases.

* Summarized data is stored in multidimensional cubes.

* Provides a balance between storage and query speed.

Example: Microsoft SQL Server Analysis Services.

Best For: Balancing storage and speed.

### Architecture / Working

![OLAP Architectures Comparison (ROLAP, MOLAP, HOLAP) - upzone - 博客园](https://images.openai.com/static-rsc-4/xfHt6BmLeqGEuHFHBFYPn9zFiOKHY5SbPClYbEFFPn83zRKxlu22owCnSpKu7EQuGv9hOWV9YERk5gxCuQx8GEUf5OBxXKDpItjeepHwI-_S_CvSbl__hP6rVO8ErnD3gsftWuQgWl7LUjkZJ9UtK1XeqtFgtXypUiIEVTeKrDmdFA1Ma2onV1QIk4iWJnzd?purpose=fullsize)

### Comparison of OLAP Servers

| Feature          | ROLAP         | MOLAP                  | HOLAP         |
| ---------------- | ------------- | ---------------------- | ------------- |
| Storage          | Relational DB | Multidimensional cubes | Both          |
| Query Speed      | Slow          | Very Fast              | Fast          |
| Scalability      | Excellent     | Limited                | Good          |
| Storage Space    | Low           | High                   | Moderate      |
| Data Aggregation | At query time | Precomputed            | Both          |
| Best For         | Huge volumes  | Fast analysis          | Balanced use  |
| Example          | MicroStrategy | Oracle Essbase         | MS SQL Server |

### Easy Way to Remember

* ROLAP: R = Relational tables.

* MOLAP: M = Multidimensional cubes.

* HOLAP: H = Hybrid (both).

Conclusion: ROLAP, MOLAP, and HOLAP are different OLAP server types used for multidimensional data analysis. They differ mainly in storage, speed, and scalability.

Reference: Uploaded Unit III notes, page 3.

### 5\. OLTP vs OLAP

### A. OLTP (Online Transaction Processing)

### Definition

OLTP is a system used to manage and process day-to-day transactions in real time.

It mainly focuses on inserting, updating, deleting, and retrieving transaction records.

Examples:

* ATM transactions.

* Online banking.

* E-commerce orders.

* Railway ticket booking.

### B. OLAP (Online Analytical Processing)

### Definition

OLAP is a system used to analyze large amounts of historical and integrated data for reporting and decision-making.

It mainly focuses on reading, analyzing, and summarizing data.

Examples:

* Monthly sales analysis.

* Business intelligence reports.

* Sales forecasting.

### Diagram

![OLTP vs. OLAP: Data Processing Patterns](https://images.openai.com/static-rsc-4/PjdG4Em1QmUe669G7CtPnMuklXJwX7s42aFLFtJ-0LC-clqutgvktcm4v-bxORDTIdhcnCbezyEoa0xBjYrkCv_dmJzuTfpdOnuCrlR0z-ECZPYOsmaeeykQ4jF0qB9e2iwV27hDTAawi34A-mqcCl-oCONQHFoJfsV2ajzHNrSe-rCZvkIRrzJav1teqyUw?purpose=fullsize)

### Difference Between OLTP and OLAP

| Feature         | OLTP                              | OLAP                              |
| --------------- | --------------------------------- | --------------------------------- |
| Full Form       | Online Transaction Processing     | Online Analytical Processing      |
| Purpose         | Day-to-day transaction processing | Data analysis and decision-making |
| Data            | Current, real-time data           | Historical, integrated data       |
| Users           | Clerks, customers, operators      | Managers, analysts, executives    |
| Operations      | Insert, Update, Delete            | Read, Analyze, Aggregate          |
| Queries         | Simple queries                    | Complex queries                   |
| Response Time   | Milliseconds                      | Seconds to minutes                |
| Database Design | Normalized (3NF)                  | Denormalized (Star/Snowflake)     |
| Data Volume     | Small to Medium                   | Very Large (GBs/TBs)              |
| Data Refresh    | Continuous                        | Periodic (batch ETL)              |
| Focus           | Transaction speed                 | Decision support                  |
| Examples        | ATM, Online Banking               | Sales Analysis, BI                |

### Real-World Example

Consider an online shopping application:

OLTP:

* Customer places an order.

* Payment is processed.

* Product stock is updated.

OLAP:

* Manager checks monthly sales.

* Identifies best-selling products.

* Compares sales across different locations.

### Easy Way to Remember

* OLTP = Transactions

* OLAP = Analysis

Conclusion: OLTP manages daily business transactions, whereas OLAP analyzes historical data to support business decisions.

Reference: Uploaded Unit III notes, page 3.

### Quick Revision Sheet – Unit III

| Topic           | Important Points to Remember                   |
| --------------- | ---------------------------------------------- |
| Data Warehouse  | Definition, SITN, three-tier architecture, ETL |
| Schema Types    | Star, Snowflake, Fact Constellation            |
| OLAP Operations | Roll-Up, Drill-Down, Slice, Dice, Pivot        |
| OLAP Servers    | ROLAP, MOLAP, HOLAP                            |
| OLTP vs OLAP    | Purpose, data, users, operations, differences  |

### Important Mnemonics

1\. Data Warehouse Characteristics – SITN

* S – Subject-Oriented

* I – Integrated

* T – Time-Variant

* N – Non-Volatile

2\. OLAP Operations – RDSDP

* R – Roll-Up

* D – Drill-Down

* S – Slice

* D – Dice

* P – Pivot

3\. OLAP Servers – RMH

* R – ROLAP

* M – MOLAP

* H – HOLAP

4\. OLTP vs OLAP

* OLTP – Transactions

* OLAP – Analysis

### Most Important Diagrams to Practice

* Three-tier Data Warehouse Architecture.

* Star, Snowflake and Fact Constellation Schemas.

* OLAP Data Cube and its five operations.

* ROLAP, MOLAP and HOLAP comparison.

Study suggestion: Learn the definition first, understand the diagram, and then memorize the components and examples. For comparison questions, practice the tables rather than memorizing separate paragraphs.
