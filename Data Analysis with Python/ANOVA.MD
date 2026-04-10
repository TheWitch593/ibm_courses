# ANOVA (Analysis of Variance)

## What Is ANOVA?

ANOVA = **Analysis of Variance**

It is a statistical method used to:
- Compare multiple groups  
- Analyze categorical variables  
- Check if groups have different impacts on a target variable  

---

## Why Do We Use ANOVA?

ANOVA helps us:
- Find correlation between categories of a categorical variable  
- Determine if differences between groups are significant  

Example:
- Does car **make** (Honda, Subaru, Jaguar) affect **price**?  

---

## What Does ANOVA Return?

ANOVA gives two important values:

### 1. F-test Score

- Measures:
  - Variation **between groups**
  - Compared to variation **within groups**

Formula idea:
F = variance_between_groups / variance_within_groups


Interpretation:
- Small F → weak correlation  
- Large F → strong correlation  

---

### 2. P-value

- Shows statistical significance  
- Indicates confidence in the result  

Interpretation:
- Small P-value (< 0.05) → strong evidence (significant)  
- Large P-value (> 0.05) → weak evidence (not significant)  

---

## Understanding F-test Intuition

### Case 1: Small F-score
- High variation inside groups  
- Small difference between group means  
- → Weak correlation  

Example:
- Honda vs Subaru (similar prices)  

---

### Case 2: Large F-score
- Big difference between group means  
- Lower variation inside groups  
- → Strong correlation  

Example:
- Honda vs Jaguar (very different prices)  

---

## Performing ANOVA in Python

### Step 1: Select Data

```python
df_anova = df[["make", "price"]]

Here are your notes, cleaned, structured, and ready to copy in **Markdown format**:

```md id="anova91"
# ANOVA (Analysis of Variance)

## What Is ANOVA?

ANOVA = **Analysis of Variance**

It is a statistical method used to:
- Compare multiple groups  
- Analyze categorical variables  
- Check if groups have different impacts on a target variable  

---

## Why Do We Use ANOVA?

ANOVA helps us:
- Find correlation between categories of a categorical variable  
- Determine if differences between groups are significant  

Example:
- Does car **make** (Honda, Subaru, Jaguar) affect **price**?  

---

## What Does ANOVA Return?

ANOVA gives two important values:

### 1. F-test Score

- Measures:
  - Variation **between groups**
  - Compared to variation **within groups**

Formula idea:
```

F = variance_between_groups / variance_within_groups

````

Interpretation:
- Small F → weak correlation  
- Large F → strong correlation  

---

### 2. P-value

- Shows statistical significance  
- Indicates confidence in the result  

Interpretation:
- Small P-value (< 0.05) → strong evidence (significant)  
- Large P-value (> 0.05) → weak evidence (not significant)  

---

## Understanding F-test Intuition

### Case 1: Small F-score
- High variation inside groups  
- Small difference between group means  
- → Weak correlation  

Example:
- Honda vs Subaru (similar prices)  

---

### Case 2: Large F-score
- Big difference between group means  
- Lower variation inside groups  
- → Strong correlation  

Example:
- Honda vs Jaguar (very different prices)  

---

## Performing ANOVA in Python

### Step 1: Select Data

```python
df_anova = df[["make", "price"]]
````

---

### Step 2: Group Data

```python
grouped_anova = df_anova.groupby("make")
```

---

### Step 3: Apply ANOVA Test

```python
from scipy import stats

stats.f_oneway(group1, group2)
```

* `group1`, `group2` → price data for each category

---

## Example Results

* Honda vs Subaru:

  * F-score → small
  * P-value > 0.05
    → No significant difference

* Honda vs Jaguar:

  * F-score → large
  * P-value < 0.05
    → Significant difference

---

## Key Insight

Strong relationship exists when:

* F-test score is **large**
* P-value is **small**

ANOVA helps identify:

* Which categories impact the target variable
* Whether differences between groups are meaningful

```

