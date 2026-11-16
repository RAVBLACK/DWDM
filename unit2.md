
# UNIT II – DATA PREPROCESSING 

# 1. Data Preprocessing – Need and Importance

## Definition

Data Preprocessing is the process of converting raw, incomplete, inconsistent, and noisy data into clean and meaningful data before applying data mining techniques.

## Need for Data Preprocessing

- **Incomplete Data:** Some records may have missing values.
- **Noisy Data:** Data may contain errors or unwanted values.
- **Inconsistent Data:** Same information may be stored in different formats.
- **Duplicate Data:** Repeated records may exist.
- **Large Data:** Large datasets require more processing time.
- **Poor Data Quality:** Incorrect data can produce misleading results.

## Major Steps in Data Preprocessing

![Data Preprocessing](https://images.openai.com/static-rsc-4/naXX1vJqme22cseKOjLOrCdBJLD8GETnaZv1b4PPy0D9rUox760OEsCDwKnzC9Hj18CYtffPYyymNjtjeNGwNpjJejvbP4KdtFdCunp9PBc6g1JWUpHlXdcNzjwNnSoBUMctISL6D1GY5vIYxTPiNN-PnMNOnQk-osRGr0sMLVLAJUWSbE6VAl6kglVPkBSM?purpose=fullsize)

### 1. Data Cleaning
- Removes missing values, errors, noise, and duplicates.
- Example: Removing duplicate student records.

### 2. Data Integration
- Combines data from multiple sources.
- Example: Combining attendance and marks records.

### 3. Data Transformation
- Converts data into a suitable format.
- Example: Converting marks into percentages.

### 4. Data Reduction
- Reduces data size while preserving important information.
- Example: Selecting a smaller sample from a large dataset.

### 5. Data Discretization
- Converts continuous values into groups.
- Example: Age → Young, Adult, Senior.

## Importance

- Improves data quality and accuracy.
- Reduces processing time.
- Removes unnecessary data.
- Improves data mining efficiency.
- Helps in better decision-making.

**Conclusion:** Data preprocessing improves the quality of input data and helps produce accurate data mining results.

## Memory Trick: Need = INIDLP

- **I** – Incomplete
- **N** – Noisy
- **I** – Inconsistent
- **D** – Duplicate
- **L** – Large data
- **P** – Poor quality

---

# 2. Descriptive Data Summarization

## Definition

Descriptive Data Summarization is the process of describing and summarizing the important characteristics of a dataset using statistical measures and graphical representations.

It helps understand large datasets easily.

## Major Techniques

There are two main categories:

![Measures of Central Tendency and Dispersion](https://images.openai.com/static-rsc-4/M5_8f-BFL_4T4iiiLBm6oWWosd6bllmWk0fq5glJrydLs3r1rFHXRjBohGsvxtVda-cEgiRywzSVYEDaIxe0P9H-LlTPAYzUiYWfYnkAL0hdIlbOPVTT6xsh0FzJHiXvAdxqKUDfRXwsiLG758skK_r5qsKuDmxkl7yx67X_mPoOU3tssYQWzf6m0THUiZLm?purpose=fullsize)

## A. Measures of Central Tendency

These measures identify the central or average value of a dataset.

### 1. Mean

Mean is the average of all values.

**Formula:**

$$
Mean = \frac{\sum x}{n}
$$

**Example:** 10, 20, 30

Mean = 60/3 = 20.

### 2. Median

Median is the middle value after arranging data in ascending or descending order.

**Example:** 10, 20, 30

Median = 20.

### 3. Mode

Mode is the value that occurs most frequently.

**Example:** 10, 20, 20, 30

Mode = 20.

## B. Measures of Dispersion

These measures describe how much data values are spread out.

### 1. Range

Difference between maximum and minimum values.

**Formula:**

$$
Range = Maximum - Minimum
$$

**Example:** 10, 20, 30

Range = 30 - 10 = 20.

### 2. Variance

Measures how far data values are spread from the mean.

**Formula:**

$$
\sigma^2 = \frac{\sum(x-\mu)^2}{N}
$$

### 3. Standard Deviation

Measures the amount of variation or spread in data.

**Formula:**

$$
\sigma = \sqrt{\frac{\sum(x-\mu)^2}{N}}
$$

- Low SD = Values are close to the mean.
- High SD = Values are widely spread.

## C. Graphical Techniques

![Histogram](https://images.openai.com/static-rsc-4/kBahPtWOwVjOUKI1gnUUc9qZ8tKUIqI_O7SdV5K48ztbYDpr9iDSw2dQyIB84VoGmoNpZEwgT4E5WJbyapkrIXDM5t0BVINd3tvztTyZCAnoWPZaqjPdi22Nc1OQ4Q41GyvtRnopNhhhEwNgSFRw0FJbn87qRX57tBqzkY83HcvMzgC8RYaHMmtZ-PyqnQEL?purpose=fullsize)

![Box Plot](https://images.openai.com/static-rsc-4/XekUriD4LyH9FUt6Lg-KiRBFFoL0DpZorMOWSWadsKe9vN4j-Jf8tFNWpp756M_v0WQO4qLU24JoQu-FCSh2j3-XxLtxcgtWU-GsmnrIbMKs2CmVHPP-BN4zrmeyU2rNToaMYka6WKxaRlEYMcZL4AHjEJ_ZB4iFLAN26YPM24RB2L8wSbb1qDUmPKDTNZaO?purpose=fullsize)

![Statistics Graphs](https://images.openai.com/static-rsc-4/ux-Fjwnb2K3mp1IszsTafORJVhn-NhVJ0K_an5R59srCgCD-FjxfeMMSWCQCXkIUE7kOVJrj_rPGyZMhYNAFM7_PrXl0Mv4iZXuI5689z1b9ZnDj5PPra8EP7RkO3oxXrS1u6YX-D8Ff1RsmfwTa6PbWue-jqsztH5Rck3UOY7I8frQdGifgHgSyvyTmUHOP?purpose=fullsize)

![Frequency Distribution](https://images.openai.com/static-rsc-4/GE-EzodZjsPIMyk-PaxpMS6DQpOPGbjMzpjd3A1x7RylVR950n7DMNQsO-AogwOToeo-nIlJgrk6QQHsxvrEblCli87H6tRkoyFh2VQcwfRr2WyudmFzIuPqQEuPVNMkLDROdFY7CGdNd4ljaIx87_vHEJkp_swF8O0UNc1aNi-3GchZv3Mu_yPuROlSmkzt?purpose=fullsize)

![Data Visualization](https://images.openai.com/static-rsc-4/1oNrIKnRpNoLkBWGyBeOwbjigneVowtPyvpUipO2do5_LDOUbG13S7je9NHpppXI4dV33zD0PEukHsrWlh_Pc6nHXdo5mlPX9FtmpEBH54uMZC70yfZAdfPXBGvfuSAuqY_RQKmXrSv26tig2vjBW4d2xIFlhM6DUJjLDPgA6CtWDuW8SfbXA5woZcTdVhWy?purpose=fullsize)

- **Histogram:** Shows frequency distribution using bars.
- **Box Plot:** Shows median, quartiles, and outliers.
- **Bar Chart:** Compares different categories.
- **Pie Chart:** Shows data in percentages.
- **Scatter Plot:** Shows relationships between two variables.

## Example

Marks = 60, 70, 70, 80, 90

| Measure | Answer |
|---|---:|
| Mean | 74 |
| Median | 70 |
| Mode | 70 |
| Range | 30 |

## Advantages

- Makes large datasets easier to understand.
- Identifies patterns and trends.
- Detects unusual values.
- Helps compare data.
- Supports decision-making.

## Memory Trick

- **Central Tendency = MMM**
  - M – Mean
  - M – Median
  - M – Mode

- **Dispersion = RVS**
  - R – Range
  - V – Variance
  - S – Standard Deviation

- **Graphs = HBPSC**
  - H – Histogram
  - B – Box Plot
  - B – Bar Chart
  - P – Pie Chart
  - S – Scatter Plot

---

# 3. Discretization and Concept Hierarchy Generation

## A. Data Discretization

### Definition

Data Discretization is the process of converting continuous numerical values into a limited number of intervals or categories.

### Need for Discretization

- Reduces the number of distinct values.
- Simplifies large datasets.
- Makes data easier to understand.
- Improves data mining efficiency.
- Converts numerical data into meaningful categories.

### Example

| Age Range | Category |
|---|---|
| 0–18 | Teenager |
| 19–35 | Young Adult |
| 36–55 | Middle-aged |
| Above 55 | Senior |

## Types of Discretization

### 1. Binning Method

Divides sorted data into groups called bins.

**Equal Width:** Each bin has the same interval width.

$$
Width = \frac{Maximum-Minimum}{Number\ of\ bins}
$$

**Equal Frequency:** Each bin contains approximately the same number of records.

**Example:** Data = 10, 20, 30, 40, 50, 60

For 3 bins:

- Bin 1: 10, 20
- Bin 2: 30, 40
- Bin 3: 50, 60

### 2. Histogram Analysis

Uses a histogram to divide data into intervals.

**Example:** Marks → 0–20, 21–40, 41–60.

### 3. Clustering-Based Discretization

Groups similar numerical values into clusters.

**Example:** Customers → Low, Medium, High spending.

### 4. Entropy-Based Discretization

Uses entropy and information gain to find suitable splitting points.

**Example:** Dividing marks into intervals to distinguish Pass and Fail students.

---

## B. Concept Hierarchy Generation

### Definition

Concept Hierarchy Generation is the process of organizing data into different levels of abstraction, from detailed values to generalized concepts.

### Need

- Simplifies complex data.
- Provides different levels of abstraction.
- Helps in data generalization.
- Makes data analysis easier.

## Examples

### 1. Location Hierarchy

![Location Hierarchy](https://images.openai.com/static-rsc-4/7rTAn-mbW4S5Ztfx85XyhrcWjH3tyI-i_Z0vqzd-Qbhyokv0ACh-C16sDx0eb2T6k6Bg6kEJwwoWQR20VpAz-jEkXdh6wj9GXE7ywcWRtKonT49gstobdvJlgNlxcLHoNHMi4eGEDj6HvMTfkbrCDWjfVtWSAUYKM7QjpdOkYTke5sDnQa1TOJq6FMyzC_t1?purpose=fullsize)

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

### 2. Age Hierarchy

```text
          Age
           |
       Age Groups
           |
    ----------------
    |      |       |
  Young  Adult   Senior
```

## Methods of Concept Hierarchy Generation

### 1. Categorical Attributes
- Groups categorical values into higher-level concepts.
- Example: City → State → Country.

### 2. Numerical Attributes
- Divides numerical values into intervals or ranges.
- Example: Age → Young, Adult, Senior.

### 3. Automatic Generation
- System automatically identifies relationships between attributes.
- Example: Street → City → State → Country.

## Advantages

- Organizes data systematically.
- Supports data generalization.
- Provides different levels of detail.
- Simplifies data analysis.

## Difference Between Discretization and Concept Hierarchy

| Discretization | Concept Hierarchy |
|---|---|
| Converts continuous values into groups. | Organizes data into abstraction levels. |
| Mainly used for numerical data. | Used for numerical and categorical data. |
| Example: Age 18–25 → Young. | Example: Hyderabad → Telangana → India. |

## Memory Trick

**Discretization Types = BHCE**

- B – Binning
- H – Histogram
- C – Clustering
- E – Entropy

**Concept Hierarchy Methods = CNA**

- C – Categorical
- N – Numerical
- A – Automatic

---

# Final Revision Sheet

| Topic | What to Memorize |
|---|---|
| Data Preprocessing | Definition, INIDLP, 5 steps, importance |
| Descriptive Summarization | MMM, RVS, HBPSC |
| Discretization | Definition, BHCE, example |
| Concept Hierarchy | Definition, CNA, location diagram |

