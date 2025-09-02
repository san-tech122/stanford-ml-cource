# Machine Learning Algorithms

## 1. Supervised Learning  
- Most used in real-world applications  
- Covered in Course 1 & 2  
- Involves training on labeled data  

## 2. Unsupervised Learning  
- Finds hidden patterns or groupings in data  
- Covered in Course 3  

## 3. Recommender Systems  
- Used in platforms like YouTube, Netflix, Amazon  
- Personalized suggestions  

## 4. Reinforcement Learning  
- Agent learns by trial & error through rewards and penalties  
- Example: self-driving cars, game AI  

---

### Extra Notes
- Machine Learning = field of study that gives computers the ability to learn without being explicitly programmed.  
- Arthur Samuel (1950s): Defined ML and created a checkers-playing program.

---

## superwised learning
- refers to algorithms that learn x to y or input to output mappings.
-  The key characteristic of supervised learning is that you give your learning algorithm examples to learn from.
for example


Supervised learning refers to algorithms that learn input → output mappings from labeled data.  

## Examples

| Input (X)         | Output (Y)               | Application          |
|-------------------|--------------------------|----------------------|
| email             | spam? (0/1)             | spam filtering       |
| audio             | text transcripts        | speech recognition   |
| English           | Spanish                 | machine translation  |
| ad, user info     | click? (0/1)            | online advertising   |
| image, radar info | position of other cars  | self-driving cars    |
| image of phone    | defect? (0/1)           | visual inspection    |

## Key Point
- **Supervised learning** = learning from labeled examples (X → Y).  
- 99% of current ML economic value is from supervised learning applications.



# Supervised Learning — Regression vs Classification

Supervised learning = learning from labeled examples (given the “right answers”).

## Regression
- **Goal:** Predict a **number** (continuous value).
- **Outputs:** **Infinitely** many possible values.
- **Examples:** house price, temperature, salary, mpg, stock return.
- **Common metrics:** MSE / RMSE / MAE, R².

## Classification
- **Goal:** Predict a **category** (class label).
- **Outputs:** **Small** finite set of values.
- **Examples:** spam/not-spam, disease vs healthy, digit 0–9, sentiment ±.
- **Common metrics:** accuracy, precision/recall/F1, ROC-AUC.

---

## Quick Contrast

| Aspect                | Regression                              | Classification                         |
|----------------------|------------------------------------------|----------------------------------------|
| Target `y`           | Continuous number                        | Discrete class (binary or multi-class) |
| Output space         | Infinite                                 | Finite (small set)                     |
| Example model types  | Linear/Polynomial Regression, SVR        | Logistic Regression, SVM, Trees, NN    |
| Loss (typical)       | MSE / MAE                                | Cross-Entropy / Log Loss               |
| Evaluation (typical) | RMSE, MAE, R²                            | Accuracy, F1, Precision, Recall, AUC   |

---

## Simple “Which one is it?” Flow

```mermaid
flowchart TD
    A[Do you want to predict a number?] -->|Yes| B[Regression]
    A -->|No, a category/label| C[Classification].