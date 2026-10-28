# UNIT-VI: Cluster Analysis and Advanced Concepts

# PART A: ALGORITHMS

## 1. DBSCAN (Density-Based Clustering)

### Definition

DBSCAN stands for Density-Based Spatial Clustering of Applications with
Noise.

It groups closely packed data points into clusters and identifies
isolated points as noise.

### Steps of Algorithm (6 points)

1.  Choose `Eps` (maximum neighborhood distance).
2.  Choose `MinPts` (minimum points required).
3.  Select an unvisited point.
4.  Find its neighbors within Eps.
5.  If enough neighbors exist, form and expand a cluster.
6.  Repeat until all points are visited; mark remaining isolated points
    as noise.

### Numerical Example

Given points:

A(1,1), B(1,2), C(2,1), D(8,8)

Take:

-   Eps = 1.5
-   MinPts = 3 (including the point itself)

Distances between A, B and C are less than 1.5.

Therefore:

-   Cluster 1 = {A, B, C}
-   Noise = {D}

**Answer:** One cluster and one noise point.

### Uses

-   Identifying customer groups
-   Detecting unusual transactions
-   Geographic data clustering
-   Identifying outliers
-   Grouping spatial data

------------------------------------------------------------------------

## 2. Grid-Based Clustering

### Definition

Grid-based clustering divides the data space into a fixed number of grid
cells and groups dense neighboring cells into clusters.

### Steps of Algorithm (6 points)

1.  Divide the data space into grid cells.
2.  Calculate the number of points in each cell.
3.  Identify cells having sufficient points.
4.  Mark dense cells.
5.  Join neighboring dense cells.
6.  Form clusters from connected dense cells.

### Numerical Example

Suppose the grid contains:

  Cell     Points
  ------ --------
  G1            4
  G2            3
  G3            1

Take minimum density = 3 points.

-   G1 is dense.
-   G2 is dense.
-   G3 is not dense.

If G1 and G2 are neighbors:

**Cluster 1 = {G1, G2}**

G3 is excluded.

### Uses

-   Geographic information systems
-   Image processing
-   Large spatial datasets
-   Fast clustering of multidimensional data

------------------------------------------------------------------------

## 3. Model-Based Clustering

### Definition

Model-based clustering assumes that data is generated from a mixture of
probability distributions.

Each cluster is represented by a statistical model.

A common method is the **Gaussian Mixture Model (GMM)**.

### Steps of Algorithm (6 points)

1.  Choose the number of clusters.
2.  Initialize the cluster parameters.
3.  Assign probabilities to each data point.
4.  Estimate the cluster parameters.
5.  Repeat assignment and estimation until convergence.
6.  Assign points to their most probable clusters.

### Numerical Example

Given data:

`2, 3, 10, 11`

Take 2 clusters.

-   Cluster 1 = {2, 3}
-   Cluster 2 = {10, 11}

Means:

\[ `\mu`{=tex}\_1=`\frac{2+3}{2}`{=tex}=2.5 \]

\[ `\mu`{=tex}\_2=`\frac{10+11}{2}`{=tex}=10.5 \]

**Answer:** Two clusters with means 2.5 and 10.5.

### Uses

-   Customer segmentation
-   Medical data analysis
-   Pattern recognition
-   Statistical data analysis
-   Image classification

------------------------------------------------------------------------

## 4. K-Means Clustering (Partitioning Method)

### Definition

K-Means is a partitioning clustering algorithm that divides data into K
clusters by assigning each point to its nearest centroid.

### Steps of Algorithm (6 points)

1.  Choose the number of clusters K.
2.  Select K initial centroids.
3.  Calculate the distance of each point from each centroid.
4.  Assign points to the nearest centroid.
5.  Calculate new centroids using cluster means.
6.  Repeat until centroids stop changing.

### Numerical Example

Given points:

`2, 4, 10, 12`

Take K = 2.

Initial centroids = 2 and 10.

-   Cluster 1 = {2, 4}
-   Cluster 2 = {10, 12}

New centroids:

\[ C_1=`\frac{2+4}{2}`{=tex}=3 \]

\[ C_2=`\frac{10+12}{2}`{=tex}=11 \]

**Answer:** Cluster 1 = {2,4}, Cluster 2 = {10,12}.

### Uses

-   Customer segmentation
-   Image compression
-   Document grouping
-   Market analysis
-   Data summarization

------------------------------------------------------------------------

## 5. Agglomerative Hierarchical Clustering

### Definition

Agglomerative clustering is a hierarchical method that starts with each
data point as a separate cluster and repeatedly merges the closest
clusters.

### Steps of Algorithm (6 points)

1.  Treat every data point as a separate cluster.
2.  Calculate distances between clusters.
3.  Find the two nearest clusters.
4.  Merge them into one cluster.
5.  Recalculate distances.
6.  Repeat until the required number of clusters is obtained.

### Numerical Example

Given:

`A = 1, B = 2, C = 8`

Distances:

-   A--B = 1
-   B--C = 6
-   A--C = 7

First merge A and B.

-   Cluster 1 = {A, B}
-   Cluster 2 = {C}

**Answer:** Two clusters: {A,B} and {C}.

### Uses

-   Biological classification
-   Document clustering
-   Customer grouping
-   Social network analysis
-   Data visualization

------------------------------------------------------------------------

# PART B: TEXT MINING VS WEB MINING

## 12 Differences

  -----------------------------------------------------------------------
  Text Mining                         Web Mining
  ----------------------------------- -----------------------------------
  1\. Extracts useful information     1\. Extracts useful information
  from text.                          from web data.

  2\. Works mainly with text          2\. Works with webpages, links and
  documents.                          web content.

  3\. Uses text classification and    3\. Uses web crawling and web
  NLP.                                analysis.

  4\. Data comes from books, emails   4\. Data comes from websites and
  and reports.                        online platforms.

  5\. Focuses on words and their      5\. Focuses on web content,
  meanings.                           structure and usage.

  6\. Uses tokenization and stemming. 6\. Uses crawling, indexing and
                                      link analysis.

  7\. Finds topics and patterns in    7\. Finds patterns in webpages and
  text.                               user activities.

  8\. Usually analyzes document       8\. Analyzes content, links and
  content.                            user behavior.

  9\. Example: analyzing customer     9\. Example: analyzing website
  reviews.                            visitors.

  10\. Helps understand opinions and  10\. Helps improve websites and
  documents.                          recommendations.

  11\. Output may be topics or        11\. Output may be web patterns or
  sentiments.                         user interests.

  12\. Used in document               12\. Used in search engines and
  classification.                     website optimization.
  -----------------------------------------------------------------------

------------------------------------------------------------------------

# PART C: 20 SHORT ANSWER QUESTIONS

## Remaining syllabus \| 2--4 Marks

## Q1. What is Cluster Analysis?

**Answer:**

Cluster analysis is a data mining technique that groups similar data
objects into clusters.

-   Objects in the same cluster are similar.
-   Objects in different clusters are dissimilar.
-   It is an unsupervised learning method.

**Example:** Grouping students based on their marks.

------------------------------------------------------------------------

## Q2. What are the main applications of Cluster Analysis?

**Answer:**

1.  Customer segmentation
2.  Image processing
3.  Medical diagnosis
4.  Document classification
5.  Fraud detection

**Example:** Grouping customers based on purchasing behavior.

------------------------------------------------------------------------

## Q3. What are the types of data used in Cluster Analysis?

**Answer:**

1.  Interval-scaled data
2.  Binary data
3.  Nominal data
4.  Ordinal data
5.  Ratio-scaled data
6.  Mixed-type data

**Example:** Age is numerical data, while gender is nominal data.

------------------------------------------------------------------------

## Q4. What is Interval-Scaled Data?

**Answer:**

Interval-scaled data is numerical data where the difference between
values is meaningful.

-   Values can be compared using differences.
-   Zero does not represent the complete absence of a quantity.

**Example:** Temperature in Celsius.

------------------------------------------------------------------------

## Q5. What is Binary Data?

**Answer:**

Binary data contains only two possible values.

Usually represented as:

-   0 = No
-   1 = Yes

**Example:** Whether a student has submitted an assignment.

Binary data can be:

-   Symmetric binary
-   Asymmetric binary

------------------------------------------------------------------------

## Q6. What is Nominal Data?

**Answer:**

Nominal data represents categories without any ordering.

-   Categories are different.
-   No category is greater or smaller than another.

**Example:** Blood group: A, B, AB, O.

------------------------------------------------------------------------

## Q7. What is Ordinal Data?

**Answer:**

Ordinal data represents categories having a meaningful order.

-   Values can be ranked.
-   Differences between ranks are not necessarily equal.

**Example:** Low, Medium, High.

------------------------------------------------------------------------

## Q8. What is Ratio-Scaled Data?

**Answer:**

Ratio-scaled data is numerical data having a meaningful zero.

-   Differences are meaningful.
-   Ratios are meaningful.

**Example:** Weight, height and distance.

A weight of 20 kg is twice a weight of 10 kg.

------------------------------------------------------------------------

## Q9. What is Mixed-Type Data?

**Answer:**

Mixed-type data contains different types of attributes in the same
dataset.

It may contain:

-   Numerical data
-   Binary data
-   Nominal data
-   Ordinal data

**Example:** A student dataset containing age, gender, grade and
attendance.

------------------------------------------------------------------------

## Q10. What is Partitioning Clustering?

**Answer:**

Partitioning clustering divides a dataset into a fixed number of
clusters.

-   Each object belongs to one cluster.
-   Objects within a cluster are similar.
-   The number of clusters is usually specified in advance.

**Examples:** K-Means and K-Medoids.

------------------------------------------------------------------------

## Q11. What is K-Medoids Clustering?

**Answer:**

K-Medoids is a partitioning method that represents each cluster using an
actual data point called a medoid.

-   Select K medoids.
-   Assign points to the nearest medoid.
-   Update medoids.
-   Repeat until clusters stabilize.

**Example:** Grouping customers using representative customer records.

**Difference from K-Means:** K-Means uses the mean as a centroid, while
K-Medoids uses an actual data point.

------------------------------------------------------------------------

## Q12. What is Density-Based Clustering?

**Answer:**

Density-based clustering forms clusters from regions having a high
concentration of data points.

-   Dense regions form clusters.
-   Sparse regions may represent noise.
-   Clusters can have irregular shapes.

**Example:** DBSCAN.

**Use:** Detecting geographic groups and outliers.

------------------------------------------------------------------------

## Q13. What is Grid-Based Clustering?

**Answer:**

Grid-based clustering divides the data space into a finite number of
cells.

-   Each cell represents a region.
-   Dense cells are identified.
-   Neighboring dense cells are combined.

**Example:** STING.

**Advantage:** Fast processing of large datasets.

------------------------------------------------------------------------

## Q14. What is Model-Based Clustering?

**Answer:**

Model-based clustering assumes that data is generated from a statistical
model.

-   Each cluster has a probability distribution.
-   Data points are assigned based on their probability.
-   Model parameters are estimated.

**Example:** Gaussian Mixture Model (GMM).

**Use:** Statistical data analysis.

------------------------------------------------------------------------

## Q15. What is Outlier Analysis?

**Answer:**

Outlier analysis identifies data objects that differ significantly from
the majority of data.

These objects are called outliers.

**Example:** A transaction of ₹1,00,000 when normal transactions are
around ₹500.

**Applications:**

-   Fraud detection
-   Network intrusion detection
-   Medical diagnosis

------------------------------------------------------------------------

## Q16. What are the types of Outliers?

**Answer:**

1.  **Global outlier:** An object that differs from the entire dataset.
2.  **Contextual outlier:** An object that is unusual in a particular
    context.
3.  **Collective outlier:** A group of objects that behaves unusually
    together.

**Example:** A high temperature may be normal in summer but unusual in
winter.

------------------------------------------------------------------------

## Q17. What is Text Mining?

**Answer:**

Text mining extracts useful information and patterns from unstructured
text.

It uses techniques such as:

-   Tokenization
-   Stemming
-   Classification
-   Sentiment analysis

**Example:** Identifying positive and negative customer reviews.

**Applications:** Email filtering, document classification and opinion
analysis.

------------------------------------------------------------------------

## Q18. What are the steps involved in Text Mining?

**Answer:**

1.  Collect text documents.
2.  Remove unnecessary words and symbols.
3.  Tokenize the text.
4.  Apply stemming or normalization.
5.  Extract useful features.
6.  Analyze the text and generate results.

**Example:** Analyzing product reviews to identify customer opinions.

------------------------------------------------------------------------

## Q19. What is Web Mining? Explain its types.

**Answer:**

Web mining extracts useful information from web-related data.

It has three main types:

1.  **Web Content Mining:** Extracts information from webpage content.
2.  **Web Structure Mining:** Analyzes links between webpages.
3.  **Web Usage Mining:** Analyzes user browsing behavior.

**Example:** A shopping website recommending products based on browsing
history.

------------------------------------------------------------------------

## Q20. What is Web Usage Mining? Explain its applications.

**Answer:**

Web usage mining analyzes user activities on websites.

It uses:

-   Browsing history
-   Click patterns
-   Website visits
-   User navigation

**Applications:**

1.  Personalized recommendations
2.  Website improvement
3.  Customer behavior analysis
4.  Targeted advertising
5.  Website navigation optimization

**Example:** YouTube recommending videos based on previously watched
videos.

------------------------------------------------------------------------

# FINAL REVISION: IMPORTANT DIFFERENCES

  Method             Main Idea
  ------------------ ----------------------------------------------------
  K-Means            Groups points using cluster means.
  K-Medoids          Groups points using actual representative objects.
  DBSCAN             Groups dense regions and identifies noise.
  Grid-Based         Groups dense neighboring grid cells.
  Model-Based        Groups data using statistical models.
  Agglomerative      Starts with individual points and merges clusters.
  Outlier Analysis   Identifies unusual data objects.
  Text Mining        Extracts patterns from text.
  Web Mining         Extracts patterns from web data.

## Important Formulas

### 1. K-Means Centroid

The centroid is the mean of all points in a cluster.

\[ C_j=`\frac{1}{n_j}`{=tex}`\sum`{=tex}\_{i=1}\^{n_j}x_i \]

Where:

-   (C_j) = centroid of cluster (j)
-   (n_j) = number of points in cluster (j)
-   (x_i) = data point

### 2. Euclidean Distance

\[ d(x,y)=`\sqrt{\sum_{i=1}^{n}(x_i-y_i)^2}`{=tex} \]

For two-dimensional points:

\[ d(x,y)=`\sqrt{(x_1-y_1)^2+(x_2-y_2)^2}`{=tex} \]

### 3. DBSCAN Terms

-   **Eps:** Neighborhood radius.
-   **MinPts:** Minimum points required for a dense region.
-   **Core point:** Has sufficient neighbors.
-   **Border point:** Near a core point but has insufficient neighbors.
-   **Noise point:** Does not belong to any cluster.

------------------------------------------------------------------------
