# Section 2: Supervised and Unsupervised Learning Concepts

## 1 Flexible vs Inflexible Methods

### (a) Large Sample Size (n), Small Number of Predictors (p)

**Flexible method: Better**

**Justification:**  
When `n` is large and `p` is small, there's enough data to estimate complex relationships without overfitting. Flexible methods can capture intricate patterns effectively.

### (b) Large Number of Predictors (p), Small Number of Observations (n)

**Flexible method: Worse**

**Justification:**  
Flexible methods are prone to overfitting in high-dimensional, low-sample-size settings. Inflexible methods, with regularization or stronger assumptions, perform better.

### (c) Highly Non-Linear Relationship Between Predictors and Response

**Flexible method: Better**

**Justification:**  
Flexible methods (e.g., trees, splines, neural networks) are well-suited to model non-linear relationships, unlike inflexible methods like linear regression.

### (d) High Error Variance (σ² = Var(ε))

**Flexible method: Worse**

**Justification:**  
High noise levels increase the risk of overfitting for flexible methods. Inflexible methods are more robust in these scenarios.

---
## 3 Bias-Variance decomposition

[02_03.png]

#### Bias² (blue, dashed): Decreases with flexibility — flexible models can fit data better.
#### Variance (red, dashed): Increases with flexibility — flexible models are more sensitive to fluctuations in the data.
#### Training Error (green, dotted): Decreases — flexible models can fit training data very well.
#### Test Error (black, solid): U-shaped curve — initially decreases due to reduced bias but increases later due to high variance (overfitting).
#### Bayes Error (purple, dash-dot): Constant — the irreducible error inherent in the data.





## 4 Real-Life Applications

### (a) Classification

**1. Email Spam Detection**  
- **Response:** Spam or Not Spam  
- **Predictors:** Text content, keywords, sender address, links, attachments  
- **Goal:** Prediction  

**2. Medical Diagnosis**  
- **Response:** Disease present or not  
- **Predictors:** Age, gender, genetic markers, blood tests, imaging  
- **Goal:** Inference  

**3. Credit Card Fraud Detection**  
- **Response:** Fraudulent or Legitimate  
- **Predictors:** Transaction amount, time, merchant, location, history  
- **Goal:** Prediction  

### (b) Regression

**1. Predicting House Prices**  
- **Response:** House price (continuous)  
- **Predictors:** Square footage, bedrooms, location, year, lot size  
- **Goal:** Prediction  

**2. Estimating Medical Costs**  
- **Response:** Healthcare cost  
- **Predictors:** Age, BMI, smoking, chronic conditions, hospital history  
- **Goal:** Prediction  

**3. Understanding Wage Determinants**  
- **Response:** Salary or hourly wage  
- **Predictors:** Education, experience, job title, industry  
- **Goal:** Inference  

### (c) Cluster Analysis

**1. Customer Segmentation in Marketing**  
- Groups based on purchasing behavior, demographics, browsing  
- Tailors marketing strategies  

**2. Image Segmentation**  
- Groups pixels by color/intensity  
- Used in medical imaging or computer vision  

**3. Social Network Analysis**  
- Detects communities via interaction patterns  
- Helps suggest connections or target content  

---

## 5 Comparison of Flexible and Inflexible Approaches

### Advantages of Very Flexible Methods
- Captures complex, non-linear relationships
- Lower bias and training error
- Performs well with large datasets

### Disadvantages of Very Flexible Methods
- High variance, overfitting risk
- Hard to interpret ("black box")
- Computationally intensive

### Advantages of Less Flexible Methods
- Lower variance, better for small/noisy data
- Easier to interpret
- Faster to train

### Disadvantages of Less Flexible Methods
- Higher bias, potential underfitting
- Less accurate for complex problems

---

## Choosing Between Flexibility Levels

### Prefer More Flexible When:
- Relationships are complex/non-linear
- Large `n` relative to `p`
- Prediction accuracy is key
- Overfitting is controlled via regularization

### Prefer Less Flexible When:
- Interpretability is important
- Small `n` or noisy data
- Relationships are linear or well-understood
- Need simplicity and robustness

---

## 6 Parametric vs Non-Parametric Methods

### Parametric Methods

**Definition:**  
Assumes a specific form for the relationship between predictors and response.

**Examples:**  
- Linear regression  
- Logistic regression  
- Linear discriminant analysis  

**Advantages:**  
- Simpler to interpret  
- Computationally efficient  
- Requires less data  
- Less prone to overfitting (in low dimensions)

**Disadvantages:**  
- Risk of model misspecification  
- Inflexible for complex patterns  

---

### Non-Parametric Methods

**Definition:**  
Makes no assumptions about the functional form; lets data shape the model.

**Examples:**  
- k-Nearest Neighbors (KNN)  
- Decision trees  
- Support Vector Machines (non-linear kernels)  
- Neural networks  
- Random forests  

**Advantages:**  
- Highly flexible  
- Fewer assumptions  

**Disadvantages:**  
- Needs more data  
- Prone to overfitting  
- Hard to interpret  
- Computationally expensive  
