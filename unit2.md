### UNIT II – DATA PREPROCESSING

The following notes are structured for 8-mark examination answers. Each topic includes a definition, explanation, important techniques, examples, advantages, and key points to remember. The language is kept simple while retaining technical terminology required for exams.

### 1\. Data Preprocessing – Need and Importance

### Definition

Data Preprocessing is the process of converting raw, incomplete, inconsistent, and noisy data into a clean and meaningful format before applying data mining techniques.

It improves the quality of data and helps produce accurate results during data analysis.

### Need for Data Preprocessing

Real-world data is often collected from different sources and may contain errors. Therefore, preprocessing is required for the following reasons:

* Incomplete Data: Some records may have missing values or attributes.

* Noisy Data: Data may contain errors, incorrect values, or unwanted information.

* Inconsistent Data: Different sources may store the same information in different formats.

* Duplicate Data: The same records may appear multiple times.

* Large Volume of Data: Large datasets require processing to improve efficiency.

* Different Data Formats: Data may be stored in databases, spreadsheets, text files, etc.

* Poor Data Quality: Incorrect or irrelevant data can produce misleading results.

### Major Steps in Data Preprocessing

![What is Data Preprocessing? | Data Basecamp](https://images.openai.com/static-rsc-4/2azJQ4k7KtKmgdGR973QEgf1gcAGspAxeJPVledYAXFeA7fF8qu_iyo6Jnz7Puz5GHoZgMonELv9D_oJHq1iyyrua0DcEVhq2QoX1Km7SwoVyVE5R0ud3hIukpx9-PCv9OAe2WyKcfsLqKIJz47vD_I2o_p7QyCkqJMXKegK7jkuWNbaKmqtVokjVhIwIN60?purpose=fullsize)

### 1\. Data Cleaning

* Removes noise, errors, and duplicate records.

* Handles missing values.

* Corrects inconsistent data.

Example: Replacing missing student marks with the average marks of the class.

### 2\. Data Integration

* Combines data from multiple sources into a single dataset.

* Removes redundancy and resolves conflicts.

Example: Combining student attendance and examination records.

### 3\. Data Transformation

* Converts data into a suitable format for mining.

* Includes normalization, aggregation, and generalization.

Example: Converting marks into a percentage or standard scale.

### 4\. Data Reduction

* Reduces the size of data while maintaining important information.

* Improves processing speed and reduces storage requirements.

Example: Using sampling to select a smaller representative dataset.

### 5\. Data Discretization

* Converts continuous numerical values into intervals or groups.

* Makes data easier to understand and analyze.

Example: Converting age into groups such as Child, Adult, and Senior.

### Importance of Data Preprocessing

* Improves data quality and accuracy.

* Reduces processing time.

* Increases the efficiency of data mining algorithms.

* Removes unwanted and duplicate information.

* Improves the reliability of discovered patterns.

* Helps in better decision-making.

### Real-World Example

Consider a college database containing student details:

* Some students have missing marks.

* Some records are duplicated.

* Attendance is stored in a separate file.

* Marks are stored in different formats.

Data preprocessing cleans missing and duplicate records, combines attendance and marks, converts data into a common format, and prepares it for student performance analysis.

Conclusion: Data preprocessing is an essential step in data mining because the quality of the results depends on the quality of the input data.

### 2\. Data Integration and Transformation

### A. Data Integration

### Definition

Data Integration is the process of combining data from multiple heterogeneous sources into a single, consistent, and unified dataset.

It provides a complete view of data by bringing information from different sources together.

### Need for Data Integration

* Data is stored in different databases and files.

* Different departments maintain separate records.

* Combining data provides complete information.

* Reduces duplicate and redundant data.

* Supports better analysis and decision-making.

### Architecture / Working of Data Integration

![What is Data Integration? The Definitive Guide | Hightouch | Hightouch](https://images.openai.com/static-rsc-4/TGLV86Y1rkaoe19lhJoJljnC6GJspGuQVd1-fjBKfmfGATQMkdpZGgIwPG5cNisDJVwOjQm_1KGR2GktAlM6-8Iw2hefujv0_xgm-RlnK1rnijvkNYzhZ0nQQ7mYnFk0N41tdc5n5MKPFRj2eeeDY6KC5zZ121b9UGp8YK_goH-w_34ukf0vsFpvKqID158m?purpose=fullsize)

Explanation:

* Data Sources: Data is collected from different sources such as databases, Excel files, and websites.

* Data Extraction: Required information is extracted from each source.

* Data Cleaning: Duplicate and inconsistent records are identified and corrected.

* Data Transformation: Data is converted into a common format.

* Data Loading: The integrated data is stored in a central database or data warehouse.

### Major Issues in Data Integration

1\. Schema Integration: Different databases may use different structures and column names.

Example: One database uses `Student_ID`, while another uses `Roll_No`.

2\. Entity Identification Problem: Identifying whether two records from different sources refer to the same real-world entity.

Example: `Rahul Kumar` and `Rahul K.` may refer to the same student.

3\. Redundancy: The same information may be stored multiple times.

Example: Customer address appearing in two databases.

4\. Data Value Conflicts: The same attribute may have different values or formats.

Example: Date stored as `12-11-2026` in one database and `11/12/2026` in another.

5\. Data Format Differences: Different systems may use different units or representations.

Example: Height stored in centimeters in one source and meters in another.

### Advantages of Data Integration

* Provides a unified view of data.

* Reduces data duplication.

* Improves data consistency.

* Supports better decision-making.

* Makes data analysis easier.

### B. Data Transformation

### Definition

Data Transformation is the process of converting data from its original format into a suitable form for data mining and analysis.

It makes data consistent, organized, and easier for algorithms to process.

### Major Data Transformation Techniques

### 1\. Smoothing

* Removes noise from data.

* Helps identify the actual patterns by reducing unwanted variations.

Example: Removing unusual fluctuations in daily temperature readings.

### 2\. Aggregation

* Combines multiple data values into a summarized form.

* Reduces the amount of data.

Example: Converting daily sales records into monthly sales totals.

### 3\. Generalization

\- Replaces low-level detailed data with higher-level concepts using concept hierarchies.

Example:

`Hyderabad → Telangana → India`

### 4\. Normalization

* Scales numerical values into a common range.

* Prevents attributes with large values from dominating the analysis.

Common methods:

a) Min-Max Normalization

Converts values into a specified range, usually 0 to 1.

v'=\\frac{v-min(A)}{max(A)-min(A)}

b) Z-Score Normalization

Uses mean and standard deviation to normalize data.

v'=\\frac{v-\\mu}{\\sigma}

Where:

* = Original value

* = Mean

* = Standard deviation

c) Decimal Scaling

Moves the decimal point according to the maximum absolute value.

v'=\\frac{v}{10^j}

Where is the smallest integer such that the maximum absolute normalized value is less than 1.

### 5\. Attribute Construction

* Creates new attributes from existing attributes.

* Helps provide more useful information for analysis.

Example: Creating an `Age` attribute using Date of Birth.

### Advantages of Data Transformation

* Converts data into a suitable format.

* Improves consistency.

* Makes data easier to analyze.

* Improves algorithm performance.

* Helps discover meaningful patterns.

### Difference Between Data Integration and Data Transformation

| Data Integration                         | Data Transformation                         |
| ---------------------------------------- | ------------------------------------------- |
| Combines data from multiple sources.     | Converts data into a suitable format.       |
| Focuses on unifying data.                | Focuses on modifying data.                  |
| Resolves redundancy and conflicts.       | Applies normalization, smoothing, etc.      |
| Example: Combining attendance and marks. | Example: Converting marks into percentages. |

### 3\. Descriptive Data Summarization

### Definition

Descriptive Data Summarization is the process of describing and summarizing the important characteristics of a dataset using statistical measures and graphical representations.

It helps users understand the overall nature, distribution, and patterns of data without examining every individual record.

### Need for Descriptive Data Summarization

* Helps understand large datasets easily.

* Identifies important characteristics of data.

* Provides a quick overview of data distribution.

* Helps identify unusual values and outliers.

* Supports comparison between different datasets.

* Helps in further data analysis and decision-making.

### Major Techniques of Descriptive Data Summarization

Descriptive data summarization mainly uses two categories:

![Statistics & Types of Statistics. What is Statistics? | by Ritu Santra | Medium](https://images.openai.com/static-rsc-4/IEf1ghFolluR2pTShMs1o4shAdO2gW7WzhAZ8HQwbNLmlT8LtId8HF9RuqAyFfYai3f0wncnjpi_34tR3bT-yYPLari95I6yOAtkUmjfZwKNERqhhnkZnNJKeAcxWm6U7MLRtW_BZivuMKfAP8kOA6waBNjPn1pPpaQLI-UoNOWgfuT3sZSVSrLWIDk4mLBM?purpose=fullsize)

### A. Measures of Central Tendency

These measures identify the central or average value of a dataset.

### 1\. Mean

Mean is the average of all values in a dataset.

Formula:

Mean = \\frac{\\sum x}{n}

Where:

* = Sum of all values.

* = Total number of values.

Example:

Marks = 60, 70, 80, 90, 100

Mean = (60 + 70 + 80 + 90 + 100) / 5

Mean = 80

### 2\. Median

Median is the middle value when all data values are arranged in ascending or descending order.

Example:

Marks = 50, 60, 70, 80, 90

Median = 70

If the number of values is even, the median is the average of the two middle values.

### 3\. Mode

Mode is the value that occurs most frequently in a dataset.

Example:

Marks = 60, 70, 70, 80, 90

Mode = 70

### B. Measures of Dispersion

These measures describe how much the data values are spread out or scattered.

### 1\. Range

Range is the difference between the maximum and minimum values.

Range = Maximum - Minimum

Example:

Marks = 40, 50, 60, 80, 90

Range = 90 - 40 = 50

### 2\. Variance

Variance measures how far the data values are spread from the mean.

Population Variance Formula:

\\sigma^2 = \\frac{\\sum(x-\\mu)^2}{N}

Where:

* = Individual value.

* = Mean.

* = Total number of values.

### 3\. Standard Deviation

Standard deviation measures the amount of variation or dispersion in a dataset.

\\sigma = \\sqrt{\\frac{\\sum(x-\\mu)^2}{N}}

A low standard deviation indicates that values are close to the mean, whereas a high standard deviation indicates that values are widely spread.

### C. Graphical Data Summarization

Graphical techniques represent data visually to make it easier to understand.

* Histogram: Displays the frequency distribution of continuous numerical data using bars.

* Box Plot: Shows minimum, maximum, median, quartiles, and possible outliers.

* Bar Chart: Compares different categories of data.

* Pie Chart: Represents data as proportions or percentages of a whole.

* Scatter Plot: Shows the relationship between two numerical variables.

### Example of Descriptive Data Summarization

Consider the marks of five students:

| Student | Marks |
| ------- | ----- |
| A       | 60    |
| B       | 70    |
| C       | 70    |
| D       | 80    |
| E       | 90    |

* Mean = 74

* Median = 70

* Mode = 70

* Range = 30

Using these values, we can understand the average performance, middle value, most common marks, and spread of student marks.

### Advantages

* Makes large datasets easier to understand.

* Helps identify patterns and trends.

* Detects unusual values.

* Supports data comparison.

* Provides a foundation for further data mining.

Conclusion: Descriptive data summarization converts large amounts of raw data into meaningful statistical and graphical information, making analysis easier and more effective.

### 4\. Data Reduction Techniques

### Definition

Data Reduction is the process of reducing the size or volume of a dataset while maintaining its important information and analytical quality.

It helps in reducing storage requirements, processing time, and computational complexity without significantly affecting the results of data mining.

### Need for Data Reduction

* Real-world datasets may contain millions of records.

* Processing large datasets requires more time and memory.

* Large datasets increase computational complexity.

* Some data may be redundant or unnecessary.

* Smaller datasets make data mining algorithms faster and more efficient.

### Major Data Reduction Techniques

![Understanding Data Reduction Patterns](https://images.openai.com/static-rsc-4/6ktXvY_ejg3vHWlaSNWxQqZepwJbKNtI6476ax_OrcAASe8CERi0CRruht8unCKK3r3pygzHptyYyVFC5VY1pasR-WfAprWiLB0FVLhWubjnzFqqRLDYpvZayuX8hlF-dUMVaPWPOH6bGA7Zs4BfN8XTMJdpfdiGmRHiDKRXRprjC6b4ind9vuv4vMJxLbA_?purpose=fullsize)

Data reduction techniques are mainly classified into the following categories:

### 1\. Data Cube Aggregation

* Data Cube Aggregation summarizes detailed data into higher-level summarized data.

* It reduces the amount of data by combining values.

* It is commonly used in data warehouses for multidimensional analysis.

Example:

Instead of storing daily sales records, we can store total monthly or yearly sales.

| Month    | Daily Sales Records | Monthly Total |
| -------- | ------------------- | ------------- |
| January  | 100, 200, 150       | 450           |
| February | 150, 250, 100       | 500           |

Here, multiple daily records are converted into monthly summaries.

### 2\. Dimensionality Reduction

* Reduces the number of attributes or features in a dataset.

* Removes irrelevant and redundant attributes.

* Helps reduce computational complexity.

Methods:

a) Attribute Subset Selection

* Selects only important attributes from the original dataset.

* Removes unnecessary features.

Example: For student performance analysis, selecting attendance, assignment marks, and examination marks while removing irrelevant attributes like phone number.

b) Principal Component Analysis (PCA)

* A statistical technique used to reduce the number of dimensions.

* Converts original attributes into a smaller set of new variables called principal components.

* Preserves as much important information (variance) as possible.

Example: Reducing 10 student performance attributes into 3 principal components.

### 3\. Numerosity Reduction

* Replaces the original large dataset with a smaller representation.

* Instead of storing all records, it stores a model or summary of the data.

Methods:

a) Parametric Methods

These methods represent data using a mathematical model.

* Regression: Uses a mathematical equation to represent the relationship between variables.

* Log-Linear Models: Represent relationships among multiple discrete variables using logarithmic models.

Example: Using a regression equation to predict house prices instead of storing every possible house-price combination.

b) Non-Parametric Methods

These methods do not assume a specific mathematical model.

* Histograms: Divide data into intervals called bins and store their frequency.

* Clustering: Groups similar records into clusters and represents them using cluster information.

* Sampling: Selects a smaller representative subset from a large dataset.

Example: Selecting 1,000 students from a dataset of 1 lakh students for analysis.

### 4\. Data Compression

* Converts data into a compact representation to reduce storage space.

* It reduces the amount of memory required to store data.

Types:

a) Lossless Compression

* Original data can be completely reconstructed.

* No information is lost during compression.

Example: ZIP files.

b) Lossy Compression

* Some information is permanently removed.

* The original data cannot be reconstructed exactly.

Example: JPEG images and MP3 audio.

### 5\. Discretization

* Converts continuous numerical values into a smaller number of intervals or categories.

* Reduces the number of distinct values.

Example:

Instead of storing exact ages:

18, 19, 20, 21, 35, 40, 65

We can group them as:

* Young: 18–25

* Middle-aged: 26–50

* Senior: Above 50

### Summary of Data Reduction Techniques

| Technique                | Main Purpose            | Example                     |
| ------------------------ | ----------------------- | --------------------------- |
| Data Cube Aggregation    | Summarizes data         | Daily sales → Monthly sales |
| Dimensionality Reduction | Reduces attributes      | PCA                         |
| Numerosity Reduction     | Reduces records         | Sampling, Clustering        |
| Data Compression         | Reduces storage space   | ZIP, JPEG                   |
| Discretization           | Reduces distinct values | Age groups                  |

### Advantages of Data Reduction

* Reduces storage requirements.

* Improves processing speed.

* Reduces computational complexity.

* Makes data mining more efficient.

* Removes unnecessary information.

* Helps handle very large datasets.

Conclusion: Data reduction makes large datasets smaller and easier to process while preserving the important information required for data mining.

### 5\. Discretization and Concept Hierarchy Generation

### A. Data Discretization

### Definition

Data Discretization is the process of converting continuous numerical values into a limited number of intervals or categories.

It replaces detailed numerical values with meaningful groups, making data easier to understand and analyze.

### Need for Discretization

* Reduces the number of distinct values.

* Simplifies large datasets.

* Makes data easier to understand.

* Helps improve the efficiency of certain data mining algorithms.

* Converts numerical data into meaningful categories.

### Example

Consider the age of students:

18, 19, 20, 22, 25, 30, 35, 45, 60

After discretization:

| Age Range | Category    |
| --------- | ----------- |
| 0–18      | Teenager    |
| 19–35     | Young Adult |
| 36–55     | Middle-aged |
| Above 55  | Senior      |

Instead of handling every individual age, the system works with meaningful categories.

### Types of Discretization Methods

### 1\. Binning Method

* Divides sorted data into a fixed number of groups called bins.

* Values within each bin are treated together.

* It is a simple method of discretization.

Types of Binning:

a) Equal-Width Binning

\- Divides the entire data range into intervals of equal width.

Width = \\frac{Maximum-Minimum}{Number\\ of\\ bins}

Example:

Data = 10, 20, 30, 40, 50, 60

For 3 bins:

* Bin 1: 10–26.67

* Bin 2: 26.67–43.33

* Bin 3: 43.33–60

b) Equal-Frequency Binning

\- Divides data into bins containing approximately the same number of records.

Example:

Data = 10, 20, 30, 40, 50, 60

For 3 bins:

* Bin 1: 10, 20

* Bin 2: 30, 40

* Bin 3: 50, 60

### 2\. Histogram Analysis

* Uses a histogram to divide data into intervals.

* Each interval represents a group of values.

* Helps identify the distribution of data.

Example: Grouping student marks into 0–20, 21–40, 41–60, 61–80, and 81–100.

### 3\. Clustering-Based Discretization

* Groups similar numerical values into clusters.

* Values belonging to the same cluster are assigned to the same category.

Example: Grouping customers based on their annual spending into low, medium, and high spending groups.

### 4\. Entropy-Based Discretization

* Uses information gain and entropy to identify suitable splitting points.

* Selects intervals that best separate different classes.

* Commonly used in supervised learning.

Example: Dividing student marks into intervals that best distinguish between Pass and Fail students.

### B. Concept Hierarchy Generation

### Definition

Concept Hierarchy Generation is the process of organizing data into different levels of abstraction, from lower-level detailed values to higher-level generalized concepts.

It helps users analyze data at different levels of detail.

### Need for Concept Hierarchy Generation

* Simplifies complex data.

* Provides different levels of abstraction.

* Helps in data generalization.

* Supports multidimensional data analysis.

* Makes data mining more efficient.

### Example 1: Location Hierarchy

![PPT - Data Mining: Concepts and Techniques — Chapter 3 — PowerPoint Presentation - ID:4256137](https://images.openai.com/static-rsc-4/2fSX4sU0kcqfaL6EDCPEctyv6mG1UkU0Koo4bqLQHYVxRcROxpXRq-esQmYohDZACD-hB7bOkYJtxUNmxgVUGSa_NTVxsFWa6ng_xcmTo6gHEK7MtnIVsuAil2IOabK-lZwzXS4Qo0mwyEt0fNHh5swZCDa3ocGhKIGYzh2IAEQ9D5AbzPkBvc0wldfzO_7D?purpose=fullsize)

A location can be organized into different levels:

```text
           Country
              |
            India
              |
            State
              |
          Telangana
              |
             City
              |
          Hyderabad
```

Here:

* Hyderabad represents the lowest-level detailed data.

* Telangana represents a higher-level concept.

* India represents a more generalized concept.

### Example 2: Age Hierarchy

```text
             Age
              |
       Age Categories
              |
    ---------------------
    |         |         |
  Young   Middle-aged  Senior
    |         |         |
  18-25     26-50      51+
```

Exact ages are generalized into meaningful age groups.

### Methods of Concept Hierarchy Generation

### 1\. Concept Hierarchy for Categorical Attributes

* Created by organizing categorical values into higher-level groups.

* Uses domain knowledge and predefined relationships.

Example:

```text
        Country
           |
        India
           |
        State
           |
      Telangana
           |
         City
           |
      Hyderabad
```

### 2\. Concept Hierarchy for Numerical Attributes

* Created by dividing numerical values into intervals or ranges.

* Usually uses discretization techniques.

Example:

```text
          Age
           |
     Age Groups
           |
    ----------------
    |      |       |
  0-18   19-35    36+
```

### 3\. Automatic Concept Hierarchy Generation

* The system automatically identifies relationships among attributes.

* It can use the number of distinct values (cardinality) to identify possible hierarchy levels.

* Attributes with fewer distinct values are often placed at higher levels of abstraction.

Example:

```text
Street → City → State → Country
```

The system can identify the hierarchy based on the relationships between attributes.

### Advantages of Concept Hierarchy Generation

* Organizes data systematically.

* Supports data generalization.

* Provides different levels of detail.

* Simplifies data analysis.

* Helps discover patterns at different abstraction levels.

### Difference Between Discretization and Concept Hierarchy Generation

| Discretization                                           | Concept Hierarchy Generation                      |
| -------------------------------------------------------- | ------------------------------------------------- |
| Converts continuous values into intervals or categories. | Organizes data into different abstraction levels. |
| Mainly focuses on numerical attributes.                  | Can handle categorical and numerical attributes.  |
| Reduces the number of distinct values.                   | Provides generalized representations of data.     |
| Example: Age 18–25 → Young.                              | Example: Hyderabad → Telangana → India.           |

Conclusion: Discretization converts continuous values into meaningful groups, whereas concept hierarchy generation organizes data into multiple levels of abstraction. Both techniques simplify data and support efficient data mining.

### Quick Revision: Unit II

| Topic                              | Most Important Points                                         |
| ---------------------------------- | ------------------------------------------------------------- |
| Data Preprocessing                 | Need, importance, 5 major steps                               |
| Data Integration & Transformation  | Issues, ETL process, normalization formulas                   |
| Descriptive Data Summarization     | Mean, Median, Mode, Range, Variance, Standard Deviation       |
| Data Reduction                     | Data cube, dimensionality, numerosity, compression            |
| Discretization & Concept Hierarchy | Binning, histogram, clustering, entropy, hierarchy generation |

### Important formulas to remember

| Formula               | Expression        |
| --------------------- | ----------------- |
| Mean                  |                   |
| Range                 | Maximum − Minimum |
| Variance              |                   |
| Standard Deviation    |                   |
| Min-Max Normalization |                   |
| Z-Score Normalization |                   |
| Equal-Width Binning   |                   |

Exam preparation suggestion: Give special attention to the diagrams for preprocessing, data integration, data reduction, and concept hierarchy. Practice the normalization formulas and descriptive statistics numericals as well.
