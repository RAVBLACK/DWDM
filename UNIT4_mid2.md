# UNIT IV: Important Exam Notes

## 1. Apriori Algorithm

### Definition
Apriori is a frequent itemset mining algorithm used to find frequently occurring items and generate association rules from transaction databases. It uses the **Apriori property** to reduce the search space.

**Apriori Property:** All non-empty subsets of a frequent itemset must also be frequent.

### Steps of Algorithm (6 Points)
1. Find the support count of each individual item.
2. Remove items below minimum support.
3. Generate candidate itemsets using the join step.
4. Remove candidates having infrequent subsets using the prune step.
5. Calculate support count and find frequent itemsets.
6. Repeat until no frequent itemsets remain and generate association rules.

### Example Numerical
Given:

| TID | Items |
|---|---|
| T1 | A, B |
| T2 | A, B |
| T3 | A, C |

Minimum support count = 2

#### Step 1: Find L1

| Item | Support count |
|---|---:|
| A | 3 |
| B | 2 |
| C | 1 |

Remove C.

`L1 = {A, B}`

#### Step 2: Find L2

| Itemset | Support count |
|---|---:|
| {A, B} | 2 |

Therefore: `L2 = {{A, B}}`

#### Step 3: Generate Association Rules

Rule 1: `A → B`

Confidence = (2 / 3) × 100 = **66.67%**

Rule 2: `B → A`

Confidence = (2 / 2) × 100 = **100%**

**Final frequent itemset:** `{A, B}`

**Strong rule:** `B → A`, if minimum confidence is 80%.

### Uses
1. Market basket analysis.
2. Finding frequently purchased products.
3. Customer buying pattern analysis.
4. Product recommendation systems.
5. Improving product placement.

---

## 2. FP-Growth Algorithm

### Definition
FP-Growth (Frequent Pattern Growth) is a frequent itemset mining algorithm used to discover frequent patterns without generating candidate itemsets. It uses a compact data structure called an **FP-tree**.

### Steps of Algorithm (6 Points)
1. Scan the database and calculate support count of each item.
2. Remove items below minimum support.
3. Arrange frequent items in descending order of support count.
4. Construct the FP-tree by inserting transactions in sorted order.
5. Generate conditional pattern bases and conditional FP-trees.
6. Mine frequent itemsets from the FP-tree.

### Example Numerical
Given:

| TID | Items |
|---|---|
| T1 | A, B |
| T2 | A, B |
| T3 | A, C |

Minimum support count = 2

#### Step 1: Find support count

| Item | Support count |
|---|---:|
| A | 3 |
| B | 2 |
| C | 1 |

Remove C.

Frequent items: `L1 = {A, B}`

#### Step 2: Construct FP-tree

Transactions after removing C:

| TID | Items |
|---|---|
| T1 | A, B |
| T2 | A, B |
| T3 | A |

FP-tree:

```text
Root
 └── A:3
      └── B:2
```

#### Step 3: Find frequent itemsets

`{A}`, `{B}`, `{A, B}`

Support counts:
- A = 3
- B = 2
- AB = 2

**Final frequent itemset:** `{A, B}`

#### Association Rules
`A → B`

Confidence = (2 / 3) × 100 = **66.67%**

`B → A`

Confidence = (2 / 2) × 100 = **100%**

### Uses
1. Market basket analysis.
2. Customer purchase pattern discovery.
3. Web usage mining.
4. Recommendation systems.
5. Mining large transaction databases.

---

## 3. Difference Between Multilevel and Multidimensional Association Rules

| Multilevel Association Rules | Multidimensional Association Rules |
|---|---|
| 1. Uses different levels of abstraction. | 1. Uses different dimensions or attributes. |
| 2. Based on concept hierarchy. | 2. Based on multiple database attributes. |
| 3. Finds general and specific rules. | 3. Finds relationships across attributes. |
| 4. Example: Food → Bakery. | 4. Example: Age → Product. |
| 5. Uses product categories and subcategories. | 5. Uses age, income, location, product, etc. |
| 6. Example: Dairy → Bread. | 6. Example: Young customers → Laptop. |
| 7. Uses uniform minimum support. | 7. Uses multiple dimensions in rule formation. |
| 8. Can use reduced support at lower levels. | 8. Can use categorical and quantitative attributes. |
| 9. Example: Milk → Bread. | 9. Example: Age=Young → Product=Laptop. |
| 10. Helps discover patterns at different abstraction levels. | 10. Helps discover relationships between different attributes. |

### Easy Memory Trick
- **Multilevel = Multiple levels** (General → Specific)
- **Multidimensional = Multiple dimensions** (Age, Income, Product)

# UNIT IV: Short Answer Questions (2–4 Marks)

# Part A: Basic Concepts of Frequent Pattern Mining

### Q1. Define Frequent Pattern Mining, Frequent Itemset and Association Rule.

**Frequent Pattern Mining:** A data mining technique used to discover frequently occurring items or relationships in a database.

**Frequent Itemset:** A group of items whose support is greater than or equal to the minimum support threshold.

Example: `{Milk, Bread}` occurring in 40% of transactions.

**Association Rule:** A relationship between itemsets represented as:

`X → Y`

Example: `Milk → Bread` means customers buying milk also tend to buy bread.

### Q2. Define Support, Confidence, Minimum Support and Minimum Confidence.

**Support:** Measures how frequently an itemset occurs in the entire database.

`Support(X) = Count(X) / N × 100`

**Confidence:** Measures how frequently Y occurs when X occurs.

`Confidence(X → Y) = Count(X ∪ Y) / Count(X) × 100`

**Minimum Support:** Minimum frequency required for an itemset to be frequent.

**Minimum Confidence:** Minimum reliability required for an association rule to be strong.

### Q3. Explain the Apriori Property, Candidate Generation and Candidate Pruning.

**Apriori Property:** All non-empty subsets of a frequent itemset must also be frequent.

**Candidate Generation:** Creates possible itemsets from previously discovered frequent itemsets.

Example: `{A}` and `{B}` generate `{A, B}`.

**Candidate Pruning:** Removes candidates having at least one infrequent subset.

Example: If `{A, B}` is infrequent, `{A, B, C}` is pruned.

### Q4. Differentiate Closed Frequent Itemset and Maximal Frequent Itemset.

| Closed Frequent Itemset | Maximal Frequent Itemset |
|---|---|
| No proper superset has the same support count. | No proper superset is frequent. |
| Preserves support information. | Does not preserve support information for all subsets. |
| Can have frequent supersets. | Cannot have frequent supersets. |
| Example: `{A,B}` has support 3 and `{A,B,C}` has support 2, so `{A,B}` is closed. | Example: `{A,B,C}` is maximal if no larger frequent itemset contains it. |

---

# Part B: Frequent Itemset Mining Methods

### Q5. Explain ECLAT Algorithm and Vertical Data Format.

**ECLAT** (Equivalence Class Clustering and bottom-up Lattice Traversal) is a frequent itemset mining algorithm that uses vertical data format and transaction ID sets to discover frequent itemsets.

**Vertical Data Format:** Stores each item with the transaction IDs in which it occurs.

Example:

| Item | TID |
|---|---|
| A | T1, T2, T3 |
| B | T2, T3 |

Support count of `{A, B}`:

`TID(A) ∩ TID(B) = {T2, T3}`

Therefore, support count = 2.

### Q6. Differentiate Apriori and FP-Growth Algorithms.

| Apriori | FP-Growth |
|---|---|
| Generates candidate itemsets. | Does not generate candidate itemsets. |
| Uses join and prune steps. | Uses FP-tree. |
| Requires repeated database scans. | Usually requires two database scans. |
| Calculates support by counting transactions. | Mines patterns using conditional pattern bases. |
| Simple but can be slower for large databases. | Efficient for large databases. |

---

# Part C: Multilevel Association Rule Mining

### Q7. Define Multilevel Association Rule Mining and Concept Hierarchy.

**Multilevel Association Rule Mining:** Discovers association rules at different levels of abstraction using a concept hierarchy.

Example:
- General: Dairy → Bakery
- Specific: Milk → Bread

**Concept Hierarchy:** Represents items from general categories to specific items.

Example:

`Food → Dairy → Milk`

It helps discover both general and specific patterns.

### Q8. Explain the Three Minimum Support Approaches in Multilevel Association Mining.

**1. Uniform Minimum Support:** Uses the same support threshold at every level.

Example: 5% for Food, Dairy and Milk.

**2. Reduced Minimum Support:** Uses lower support thresholds at lower levels.

Example: Food = 10%, Dairy = 5%, Milk = 2%.

**3. Item-Based Minimum Support:** Assigns different support thresholds to different items or groups.

Example: Dairy = 10%, premium products = 2%.

---

# Part D: Multidimensional Association Rule Mining

### Q9. Define Multidimensional Association Rule Mining and Explain Its Types.

**Definition:** Multidimensional association rule mining discovers relationships between different attributes or dimensions of a database.

Example:

`Age = Young AND Income = High → Product = Laptop`

**Types:**

1. **Inter-dimensional:** Different dimensions appear once.

   Example: `Age → Product`

2. **Intra-dimensional:** Repeated predicates from the same dimension.

   Example: `Product = Laptop → Product = Mouse`

3. **Hybrid-dimensional:** Contains repeated and different dimensions.

   Example: `Age = Young AND Product = Laptop → Product = Mouse`

### Q10. Explain Quantitative Association Rules and Static Discretization.

**Quantitative Association Rules:** Rules involving numerical attributes such as age, income, price and quantity.

Example:

`Age = 20–30 AND Income = 50,000–80,000 → Laptop`

**Static Discretization:** Converts numerical values into fixed intervals before mining.

Example:
- 0–17: Young
- 18–35: Adult
- 36–55: Middle-aged

**Methods:**

1. Equal-width partitioning: Divides values into intervals of equal width.
2. Equal-frequency partitioning: Divides values into intervals containing approximately equal numbers of records.

---

# Part E: Correlation Analysis

### Q11. Define Correlation Analysis and Explain Its Types.

**Correlation Analysis:** A statistical technique used to measure the strength and direction of relationships between variables.

**Types:**

1. Positive correlation: Both variables increase or decrease together.

   Example: Study hours and marks.

2. Negative correlation: One variable increases while the other decreases.

   Example: Price and demand.

3. Zero correlation: No clear linear relationship.

   Example: Shoe size and examination marks.

### Q12. Define Lift and Explain Its Interpretation.

Lift measures how frequently two items occur together compared to what is expected if they were independent.

`Lift(X → Y) = Confidence(X → Y) / Support(Y)`

**Interpretation:**
- Lift > 1: Positive association.
- Lift = 1: Independent.
- Lift < 1: Negative association.

Example: Lift = 1.5 indicates positive association.

### Q13. Differentiate Association Mining and Correlation Analysis.

| Association Mining | Correlation Analysis |
|---|---|
| Finds frequent patterns. | Measures relationships between variables. |
| Uses support and confidence. | Uses lift and correlation measures. |
| Identifies co-occurrence. | Evaluates dependence. |
| Example: Bread → Milk. | Example: Bread and Milk have positive association. |

### Q14. Why is Correlation Analysis Needed in Association Mining?

Association mining may generate rules with high confidence even when the relationship is not interesting.

Correlation analysis checks whether items occur together more or less frequently than expected.

**Example:** If most customers purchase Bread, the rule `Bread → Milk` may have high confidence simply because Bread is frequently purchased.

Lift helps determine whether the relationship is stronger than expected.

---

# Part F: Constraint-Based Association Mining

### Q15. Define Constraint-Based Association Mining and State Its Advantages.

**Definition:** Constraint-based association mining discovers association rules that satisfy user-defined conditions.

Example: Find rules involving laptops with minimum support 20% and confidence 70%.

**Advantages:**
1. Reduces unnecessary rules.
2. Saves computational effort.
3. Improves mining efficiency.
4. Finds relevant patterns.
5. Reduces the search space.

### Q16. Explain the Types of Constraints in Association Mining.

1. **Knowledge-type constraint:** Specifies the type of pattern.

   Example: Association rules.

2. **Data constraint:** Specifies the data to be mined.

   Example: Sales data from 2025.

3. **Dimension/level constraint:** Specifies attributes or hierarchy levels.

   Example: Electronics → Mobile Phones.

4. **Interestingness constraint:** Specifies minimum or maximum support and confidence.

   Example: Support ≥ 20%.

5. **Rule constraint:** Specifies the structure of a rule.

   Example: Laptop must appear in the consequent.

### Q17. Differentiate Data Constraint, Dimension Constraint and Rule Constraint.

| Data Constraint | Dimension Constraint | Rule Constraint |
|---|---|---|
| Specifies which records to use. | Specifies which attributes or levels to use. | Specifies the required rule structure. |
| Example: 2025 sales. | Example: Age and Product. | Example: Laptop on RHS. |

### Q18. What is an Interestingness Constraint? Give an Example.

An interestingness constraint specifies minimum or maximum values of measures used to evaluate association rules.

Example:

`Support ≥ 20%`

`Confidence ≥ 70%`

A rule satisfying both conditions is considered eligible for selection.

---

# Part G: Combined Important Questions

### Q19. Explain the Difference Between Inter-Dimensional, Intra-Dimensional and Hybrid-Dimensional Rules.

| Inter-Dimensional | Intra-Dimensional | Hybrid-Dimensional |
|---|---|---|
| Uses different dimensions. | Uses repeated predicates from the same dimension. | Uses repeated and different dimensions. |
| Each dimension appears once. | Same dimension appears multiple times. | Some dimensions repeat. |
| Example: Age → Product. | Example: Laptop → Mouse. | Example: Age AND Laptop → Mouse. |

### Q20. Explain the Applications of Association and Correlation Mining.

1. **Market Basket Analysis:** Identifies products purchased together.
2. **Recommendation Systems:** Suggests related products.
3. **Customer Analysis:** Finds customer buying patterns.
4. **Retail Management:** Helps improve product placement.
5. **Web Usage Mining:** Identifies frequently visited pages.
6. **Business Decision Making:** Helps understand relationships between products and customer attributes.

---


