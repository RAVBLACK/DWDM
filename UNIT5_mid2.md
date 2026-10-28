# UNIT-V: Classification and Prediction
**Data Mining | Exam Preparation Notes**

This unit is divided into:
- **Part A:** 5 important algorithms
- **Part B:** 20 short-answer questions (2–4 marks)

---

# PART A: ALGORITHMS

## 1. Decision Tree Induction

### Definition
A Decision Tree is a classification algorithm that represents decisions in the form of a tree. It uses conditions to divide data into groups and predicts the class at the leaf node.

- Root node: First condition
- Internal node: Decision or test
- Branch: Result of a condition
- Leaf node: Final class

### Steps of the Algorithm (6)
1. Start with the entire training dataset.
2. Select the best attribute for splitting.
3. Create a decision node using that attribute.
4. Divide the data based on its values.
5. Repeat splitting until the data is classified or no useful split remains.
6. Use the leaf node to predict the class of new data.

### Numerical Example
| Weather | Play |
|---|---|
| Sunny | No |
| Sunny | No |
| Rainy | Yes |
| Rainy | Yes |

Decision:
- Weather = Sunny → Play = No
- Weather = Rainy → Play = Yes

**Prediction:** If Weather = Sunny, Play = No. If Weather = Rainy, Play = Yes.

### Uses
- Medical diagnosis
- Loan approval
- Customer classification
- Decision-making systems

---

## 2. Naive Bayes Classification

### Definition
Naive Bayes is a probabilistic classification algorithm based on Bayes' theorem. It assumes that all features are independent of each other given the class.

Formula:

$$
P(C|X)=\frac{P(X|C)P(C)}{P(X)}
$$

Where:
- \(P(C|X)\): Probability of class given data
- \(P(X|C)\): Probability of data given class
- \(P(C)\): Prior probability
- \(P(X)\): Evidence

### Steps of the Algorithm (6)
1. Collect the training dataset.
2. Identify the possible classes.
3. Calculate the prior probability of each class.
4. Calculate the probability of each feature for every class.
5. Apply Bayes' theorem to calculate class probabilities.
6. Select the class with the highest probability.

### Numerical Example
Given:
- 2 spam emails out of 10
- 8 non-spam emails out of 10
- Word "offer" appears in 2 spam emails
- Word "offer" appears in 1 non-spam email

$$
P(Spam)=\frac{2}{10}=0.2
$$

$$
P(Offer|Spam)=\frac{2}{2}=1
$$

$$
P(Offer|NotSpam)=\frac{1}{8}=0.125
$$

Spam score:

$$
1 \times 0.2=0.2
$$

Non-spam score:

$$
0.125 \times 0.8=0.1
$$

**Prediction: Spam**, because 0.2 > 0.1.

### Uses
- Email spam detection
- Text classification
- Sentiment analysis
- Medical diagnosis

---

## 3. Support Vector Machine (SVM)

### Definition
SVM is a supervised learning algorithm that classifies data by finding the best separating boundary called a hyperplane.

It selects the hyperplane with the **maximum margin**, meaning the maximum distance between the boundary and the nearest data points.

### Steps of the Algorithm (6)
1. Collect labeled training data.
2. Represent the data as points.
3. Identify possible separating hyperplanes.
4. Find the hyperplane with maximum margin.
5. Use support vectors to determine the boundary.
6. Classify new data based on which side of the boundary it lies.

### Numerical Example
Suppose:
- Class A points: 1, 2
- Class B points: 4, 5

The separating boundary is:

$$
x=3
$$

For new data:
- If x = 2 → Class A
- If x = 4 → Class B

### Uses
- Face recognition
- Image classification
- Text classification
- Disease detection

---

## 4. Backpropagation

### Definition
Backpropagation is a supervised learning algorithm used to train neural networks. It calculates the error between actual and predicted output and sends the error backward to update weights.

### Steps of the Algorithm (6)
1. Initialize network weights randomly.
2. Give input data to the network.
3. Calculate output using forward propagation.
4. Calculate error between actual and predicted output.
5. Propagate error backward and update weights.
6. Repeat until the error becomes small.

### Numerical Example
Given:
- Input = 1
- Weight = 0.5
- Actual output = 1
- Learning rate = 0.1
- Predicted output = 0.5

Error:

$$
Error=1-0.5=0.5
$$

Weight update (simple linear example):

$$
w_{new}=w+\eta Error(Input)
$$

$$
w_{new}=0.5+0.1(0.5)(1)
$$

$$
\boxed{w_{new}=0.55}
$$

The weight increases from 0.5 to 0.55 to reduce the error.

### Uses
- Image recognition
- Speech recognition
- Neural networks
- Pattern classification

---

## 5. K-Nearest Neighbor (KNN)

### Definition
KNN is a supervised classification algorithm that classifies a new data point based on the majority class of its K nearest neighbors.

It uses distance to identify the nearest points.

Euclidean distance:

$$
d=\sqrt{(x_2-x_1)^2+(y_2-y_1)^2}
$$

### Steps of the Algorithm (6)
1. Select the value of K.
2. Store the training data.
3. Calculate the distance between new data and training points.
4. Sort the distances in ascending order.
5. Select the K nearest neighbors.
6. Assign the majority class to the new data.

### Numerical Example
Training points:

| Point | Position | Class |
|---|---:|---|
| A | 1 | Red |
| B | 2 | Red |
| C | 5 | Blue |

New point = 3. Take K = 2.

Distances:
- A: |3 − 1| = 2
- B: |3 − 2| = 1
- C: |3 − 5| = 2

Two nearest points are B and A (or C in the tie, depending on tie-breaking).

**Prediction: Red**, using A and B as the two nearest neighbors.

### Uses
- Recommendation systems
- Image recognition
- Pattern recognition
- Medical classification

---

# PART B: SHORT ANSWER QUESTIONS (20)

**Remaining syllabus | 2–4 marks each**

## Q1. What is Classification?
**Definition:** Classification is a supervised learning technique that assigns data to predefined classes based on training data.

**Example:** Classifying emails as Spam or Not Spam.

**Types:** Binary classification and multiclass classification.

## Q2. What is Prediction?
**Definition:** Prediction is the process of estimating an unknown or future value using existing data.

**Example:** Predicting next month's sales using previous sales data.

**Difference:** Classification predicts a class label, while prediction commonly estimates a numerical value.

## Q3. What are the issues regarding Classification and Prediction?
Important issues are:
1. Data quality: Missing or incorrect data.
2. Overfitting: Model performs well on training data but poorly on new data.
3. Underfitting: Model fails to learn important patterns.
4. Feature selection: Choosing relevant attributes.
5. Accuracy: Measuring correct predictions.
6. Scalability: Handling large datasets efficiently.

## Q4. What is Decision Tree Induction?
Decision Tree Induction is the process of constructing a decision tree from training data.

- It selects the best attribute for splitting.
- It divides data into smaller groups.
- It continues until a stopping condition is reached.
- It uses leaf nodes for classification.

**Example:** Weather → Sunny → No Play.

## Q5. What is Entropy?
Entropy measures the impurity or uncertainty in a dataset.

Formula:

$$
Entropy(S)=-\sum p_i\log_2p_i
$$

**Example:** A dataset containing only Yes records has entropy 0 because it is completely pure. A dataset containing equal Yes and No records has entropy 1.

## Q6. What is Information Gain?
Information Gain measures the reduction in entropy after splitting a dataset using an attribute.

Formula:

$$
IG(A)=Entropy(S)-Entropy(S|A)
$$

**Example:** If parent entropy = 1 and child entropy = 0.5,

$$
IG=1-0.5=0.5
$$

The attribute provides 0.5 information gain.

## Q7. What is Gini Index?
Gini Index measures the impurity of a dataset. It is used in decision tree algorithms to select splitting attributes.

Formula:

$$
Gini(S)=1-\sum p_i^2
$$

**Example:** For 50% Yes and 50% No:

$$
Gini=1-(0.5^2+0.5^2)=0.5
$$

Lower Gini means a purer split.

## Q8. What is Bayesian Classification?
Bayesian Classification is a statistical classification method based on Bayes' theorem.

It calculates the probability of a class given the observed data.

**Example:** Using the words in an email to calculate whether it is Spam.

**Advantages:** Simple, fast, and useful for text classification.

## Q9. What is the difference between Naive Bayes and Bayesian Classification?

| Bayesian Classification | Naive Bayes |
|---|---|
| General probability-based classification approach | Specific Bayesian classifier |
| Does not necessarily assume feature independence | Assumes conditional independence of features |
| Can use different probability models | Uses the independence assumption to simplify calculations |

## Q10. What is a Support Vector Machine?
SVM is a supervised learning algorithm that separates classes using a maximum-margin hyperplane.

**Important terms:**
- Hyperplane: Decision boundary
- Margin: Distance between boundary and nearest points
- Support vectors: Nearest points that determine the boundary

**Example:** Separating spam and non-spam emails.

## Q11. What is Kernel Trick in SVM?
The Kernel Trick helps SVM classify data that cannot be separated using a straight line.

It transforms the data into a higher-dimensional space without explicitly calculating the transformation.

**Common kernels:**
1. Linear
2. Polynomial
3. RBF
4. Sigmoid

**Example:** Separating circularly distributed data.

## Q12. What is Backpropagation?
Backpropagation is a neural network training method that calculates output error and propagates it backward to update weights.

**Steps:**
1. Forward propagation
2. Calculate error
3. Backward propagation
4. Update weights

**Example:** Training a neural network to recognize handwritten digits.

## Q13. What is the Learning Rate?
Learning rate is a parameter that controls how much the weights change during training.

Formula:

$$
w_{new}=w_{old}-\eta\frac{\partial E}{\partial w}
$$

Where:
- \(w\): Weight
- \(\eta\): Learning rate
- \(E\): Error

**Example:** A learning rate of 0.1 means a smaller update than 0.5 for the same gradient.

## Q14. What is KNN Classification?
KNN classifies new data based on the majority class of its nearest neighbors.

**Important points:**
- K represents the number of neighbors.
- Distance is used to find neighbors.
- Majority voting determines the class.

**Example:** If 3 nearest neighbors contain 2 Red and 1 Blue, the new point is classified as Red.

## Q15. What is the importance of choosing K in KNN?
The value of K affects classification accuracy.

- Small K: Sensitive to noise and may overfit.
- Large K: May ignore local patterns and underfit.
- Odd K: Often used for binary classification to reduce voting ties.

**Example:** K = 3 means the algorithm considers the 3 nearest points.

## Q16. What are the Other Classification Methods?
Other classification methods include:
1. Random Forest: Uses multiple decision trees.
2. Logistic Regression: Predicts class probability.
3. Rule-Based Classification: Uses IF-THEN rules.
4. Neural Networks: Learn complex patterns.
5. Ensemble Classification: Combines multiple classifiers.

**Example:** Random Forest classifies a patient using multiple decision trees.

## Q17. What is Regression?
Regression is a supervised learning technique used to predict continuous numerical values.

**Example:** Predicting house prices based on area.

**Types:**
- Linear Regression
- Multiple Regression
- Polynomial Regression

**Difference:** Classification predicts categories, while regression predicts numerical values.

## Q18. What is Classifier Accuracy?
Classifier accuracy measures the percentage of correctly classified instances.

Formula:

$$
Accuracy=\frac{Correct\ Predictions}{Total\ Predictions}\times100
$$

**Example:** Out of 100 records, 90 are correctly classified.

$$
Accuracy=\frac{90}{100}\times100=90\%
$$

## Q19. Explain Confusion Matrix.
A confusion matrix is a table used to evaluate the performance of a classification model.

| | Predicted Positive | Predicted Negative |
|---|---|---|
| Actual Positive | TP | FN |
| Actual Negative | FP | TN |

- TP: Correctly predicted positive
- TN: Correctly predicted negative
- FP: Incorrectly predicted positive
- FN: Incorrectly predicted negative

**Example:** A model correctly identifies 10 sick patients as sick. These are True Positives.

## Q20. Explain Precision, Recall and F1-Score.
These measures evaluate classification performance.

### Precision
Measures how many predicted positive cases are actually positive.

$$
Precision=\frac{TP}{TP+FP}
$$

### Recall
Measures how many actual positive cases are correctly identified.

$$
Recall=\frac{TP}{TP+FN}
$$

### F1-Score
Harmonic mean of Precision and Recall.

$$
F1=\frac{2PR}{P+R}
$$

**Example:**

TP = 8, FP = 2, FN = 2

$$
Precision=\frac{8}{10}=0.8
$$

$$
Recall=\frac{8}{10}=0.8
$$

$$
F1=0.8
$$

---

# Final Exam Revision

## Algorithms: Remember these keywords

| Algorithm | Main keyword |
|---|---|
| Decision Tree | Splitting attributes |
| Naive Bayes | Probability |
| SVM | Maximum margin |
| Backpropagation | Error and weight update |
| KNN | Nearest neighbors |

## Important formulas

| Topic | Formula |
|---|---|
| Entropy | \(-\sum p_i\log_2p_i\) |
| Information Gain | Parent Entropy − Child Entropy |
| Gini Index | \(1-\sum p_i^2\) |
| Bayes Theorem | \(P(C|X)=\frac{P(X|C)P(C)}{P(X)}\) |
| Euclidean Distance | \(\sqrt{\sum(x_i-y_i)^2}\) |
| Accuracy | \(\frac{TP+TN}{TP+TN+FP+FN}\times100\) |
| Precision | \(\frac{TP}{TP+FP}\) |
| Recall | \(\frac{TP}{TP+FN}\) |
| F1-Score | \(\frac{2PR}{P+R}\) |
