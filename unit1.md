# 1. Data Warehouse

A Data Warehouse is a **subject-oriented, integrated, time-variant, and non-volatile collection of data** that supports the decision-making process.

Data Warehousing is the process of collecting, storing, integrating, and managing large volumes of data from multiple heterogeneous sources into a central repository.

### Characteristics of Data Warehouse

- **Subject-Oriented:** Organized around key subjects like customers, products, or sales (not around applications).
- **Integrated:** Combines data from different heterogeneous sources into a consistent format.
- **Time-Variant:** Stores historical data over long periods to identify trends.
- **Non-Volatile:** Once entered, data is not changed or deleted; only loaded and accessed.

---

# 2. Data Mining

Data Mining refers to extracting or mining knowledge from large amounts of data.

It is the process of discovering interesting knowledge, patterns, and relationships from large amounts of data stored in databases, data warehouses, or other information repositories.

# 3. KDD (Knowledge Discovery in Databases)

KDD is the process of discovering useful, valid, and understandable patterns or knowledge from large amounts of data.

## Steps in the KDD Process

### Step 1: Data Collection
- Gather raw data from various sources such as databases, files, sensors, or the internet.

### Step 2: Data Cleaning (Preprocessing)
- Removes noise and inconsistencies from data.
- Handles missing values.
- Eliminates duplicate records.
- Improves data quality.

**Example:** Removing duplicate student entries from a college database.

### Step 3: Data Integration
- Combines data from multiple sources into a unified view.
- Resolves data conflicts and redundancies.

**Example:** Combining attendance records and examination records.

### Step 4: Data Selection
- Selects only the relevant data needed for analysis.
- Reduces unnecessary data and improves mining efficiency.

**Example:** Selecting only final-year student records for placement analysis.

### Step 5: Data Transformation
- Converts data into suitable forms for mining.
- Performs normalization and aggregation.

**Example:** Converting marks into grades (A, B, C).

### Step 6: Data Mining (Core Step)
- Uses intelligent techniques to discover patterns, relationships, trends, and rules.
- Common tasks: Classification, Clustering, Association Analysis, Prediction.

**Example:** Predicting whether a student will pass or fail.

### Step 7: Pattern Evaluation
- Identifies interesting and useful patterns.
- Removes irrelevant or redundant patterns.
- Measures the significance of discovered knowledge.

### Step 8: Knowledge Presentation
- Presents discovered knowledge in an understandable form using visualization tools, graphs, charts, and reports.

# 4. Architecture of Data Mining Systems

## Overview
A Data Mining System Architecture describes the major components involved in the data mining process and how they interact to discover useful knowledge.

## 6 Major Components

### 1. Database / Data Warehouse / Information Repository
- **Sources:** Relational DBs, Data Warehouses, Transaction DBs, Flat Files, WWW, Multimedia DBs.
- **Function:** Stores large volumes of data, provides data for mining, and maintains historical and current records.
- **Example:** A supermarket database with customer purchases and sales transactions.

### 2. Database / Data Warehouse Server
- **Function:** Acts as an interface between the data mining system and data repository.
- Retrieves relevant data based on user requests.
- Performs query processing.
- **Example:** An SQL Server retrieving sales records for analysis.

### 3. Knowledge Base
- **Contents:** Data dictionaries, concept hierarchies, user beliefs, constraints, metadata, and previously discovered patterns.
- **Function:** Guides the search process and helps evaluate the interestingness of patterns.
- **Example:** Hierarchy: City → State → Country (allows mining at different abstraction levels).

### 4. Data Mining Engine (Core Component)
Performs various mining tasks:

- **Characterization:** Summarizes general features of data.
- **Discrimination:** Compares features between classes.
- **Association Analysis:** Finds relationships (Milk → Bread).
- **Classification:** Assigns objects to predefined classes.
- **Prediction:** Predicts future values.
- **Clustering:** Groups similar objects together.
- **Outlier Analysis:** Identifies exceptional patterns.
- **Evolution Analysis:** Studies trends and changes over time.

### 5. Pattern Evaluation Module
- **Function:** Identifies truly interesting patterns.
- Applies interestingness measures (Support, Confidence, Accuracy).
- Filters unimportant patterns.

### 6. Graphical User Interface (GUI)
- **Function:** Provides interaction between the user and the data mining system.
- Allows users to define mining tasks, specify parameters, view results, and visualize knowledge.
- **Features:** Charts, Graphs, Tables, Reports, Interactive dashboards.

![Data Mining Architecture](https://almablog-media.s3.ap-south-1.amazonaws.com/image1_4f42d10e91.png)

# 5. Data Mining Functionalities

## Definition
Data mining functionalities are used to specify the kind of patterns to be found in data mining tasks.

Data mining tasks are classified into two categories:

- **Descriptive Mining:** Describes what is happening within the data without a previous idea (e.g., Clustering, Association).
- **Predictive Mining:** Predicts future values using historical data (e.g., Classification, Regression).

---

## i. Concept / Class Description: Characterization & Discrimination

**Exam Tip:** Both characterization and discrimination are asked together in 5-mark questions.

### (a) Data Characterization
A summarization of the general characteristics or features of a target class of data.

**Example:**

Target class = Students who scored above 80%.

Characterization:
- Most are from AIML.
- Average CGPA > 8.5.
- Attendance > 85%.

### (b) Data Discrimination
A comparison of general features of a target class with contrasting classes.

**Example:**

| Passed Students | Failed Students |
|---|---|
| Attendance > 85% | Attendance < 60% |
| Regular assignments | Incomplete assignments |
| Higher study hours | Lower study hours |
| Active in class | Less participation |

---

## ii. Mining Frequent Patterns, Association & Correlations

### (a) Frequent Pattern Mining
The process of discovering patterns, itemsets, and subsequences that appear frequently in a dataset.

- **Frequent Itemsets:** Used in market basket analysis.
  - Example: `{Milk, Bread}`
- **Sequential Patterns:** Order matters.
  - Example: `Login → Search → Purchase`
- **Frequent Substructures:** Graphs/trees used in chemical compounds and web structures.

### (b) Association
Identifying relationships between various items.

**Example:** Used to determine which items are frequently purchased together.

### (c) Correlation Analysis
A mathematical technique showing how strongly a pair of attributes are related.

- **Positive Correlation:** Both variables increase/decrease together.
  - Example: Temperature ↑ → Ice-cream sales ↑
- **Negative Correlation:** One increases while the other decreases.
  - Example: Price ↑ → Demand ↓
- **No Correlation:** No relationship between variables.

---

## iii. Classification and Regression

### (a) Classification
The process of finding a model that distinguishes data items into predefined classes.

**Examples:**
- Email → Spam / Not Spam
- Student → Pass / Fail
- Patient → Disease / No Disease

**Algorithms:**
- Decision Tree
- Naïve Bayes
- k-NN
- SVM
- Neural Networks

### (b) Regression
A predictive technique used to predict continuous numerical values (numeric prediction).

**Examples:**
- Predict house price.
- Predict student marks.

**Algorithms:**
- Linear Regression
- Multiple Linear Regression

---

## iv. Cluster Analysis

A data mining technique used to group similar data objects into clusters, such that objects within the same cluster are more similar to each other than to those in other clusters.

It is an **unsupervised learning method** because there are no predefined class labels.

- Objects are clustered by maximizing intraclass similarity and minimizing interclass similarity.

### Types of Clustering

1. **Partitioning Methods:** Divide data into k clusters.
   - Examples: K-Means, K-Medoids.

2. **Hierarchical Methods:** Create a tree-like structure (dendrogram).
   - Agglomerative: Bottom-up approach.
   - Divisive: Top-down approach.

3. **Density-Based Methods:** Form clusters based on data density.
   - Example: DBSCAN.

---

## v. Outlier Analysis

Identifies data objects that significantly deviate from the normal behavior of the dataset.

Such objects are called **outliers or anomalies**.

**Example:**

Student marks:

- A = 65
- B = 68
- C = 70
- D = 72
- E = 15

Here, **15 is an outlier** because it significantly differs from the other values.
