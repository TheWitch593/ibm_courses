# Advanced Correlation: Pearson Correlation

## What Is Pearson Correlation?

Pearson correlation is a method used to measure:
- The **strength**
- And **direction**  
of the relationship between two continuous numerical variables  

---

## What Does It Return?

Pearson correlation gives two values:

### 1. Correlation Coefficient (r)

- Measures strength and direction of correlation  

Interpretation:
- r ≈ 1 → strong positive correlation  
- r ≈ -1 → strong negative correlation  
- r ≈ 0 → no correlation  

---

### 2. P-value

- Measures the **certainty** of the correlation  

Interpretation:
- p < 0.001 → very strong certainty  
- 0.001 < p < 0.05 → moderate certainty  
- 0.05 < p < 0.1 → weak certainty  
- p > 0.1 → no certainty  

---

## When Is Correlation Strong?

A strong correlation exists when:
- Correlation coefficient is close to **1 or -1**  
- P-value is **very small (usually < 0.001)**  

---

## Example

- Variables: Horsepower vs Price  

Results:
- Correlation coefficient ≈ 0.8 → strong positive correlation  
- P-value < 0.001 → high certainty  

Conclusion:
- Horsepower is a strong predictor of price  

---

## Calculating in Python

```python
from scipy import stats

stats.pearsonr(df["var1"], df["var2"])

Here are your notes, clean and ready to copy in **Markdown format**:

````md id="pearson77"
# Advanced Correlation: Pearson Correlation

## What Is Pearson Correlation?

Pearson correlation is a method used to measure:
- The **strength**
- And **direction**  
of the relationship between two continuous numerical variables  

---

## What Does It Return?

Pearson correlation gives two values:

### 1. Correlation Coefficient (r)

- Measures strength and direction of correlation  

Interpretation:
- r ≈ 1 → strong positive correlation  
- r ≈ -1 → strong negative correlation  
- r ≈ 0 → no correlation  

---

### 2. P-value

- Measures the **certainty** of the correlation  

Interpretation:
- p < 0.001 → very strong certainty  
- 0.001 < p < 0.05 → moderate certainty  
- 0.05 < p < 0.1 → weak certainty  
- p > 0.1 → no certainty  

---

## When Is Correlation Strong?

A strong correlation exists when:
- Correlation coefficient is close to **1 or -1**  
- P-value is **very small (usually < 0.001)**  

---

## Example

- Variables: Horsepower vs Price  

Results:
- Correlation coefficient ≈ 0.8 → strong positive correlation  
- P-value < 0.001 → high certainty  

Conclusion:
- Horsepower is a strong predictor of price  

---

## Calculating in Python

```python
from scipy import stats

stats.pearsonr(df["var1"], df["var2"])
````

* Returns: (correlation coefficient, p-value)

---

## Correlation Heatmap

A heatmap is used to visualize correlations between multiple variables.

### Features:

* Colors represent strength of correlation
* Strong correlation → darker color
* Weak correlation → lighter color

---

## Important Observation

* Diagonal values = 1
* Because each variable is perfectly correlated with itself

---

## Why Use Heatmaps?

* Quickly see relationships between variables
* Identify important predictors
* Understand how variables relate to the target (e.g., price)

---

## Key Insight

Pearson correlation helps you:

* Measure relationships between variables
* Evaluate strength and reliability
* Support feature selection in models

