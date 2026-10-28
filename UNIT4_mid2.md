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
