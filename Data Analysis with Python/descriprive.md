# Descriptive Statistics in EDA

## Why Descriptive Statistics?

Before building complex models, you should first **explore your data**.

Descriptive statistics help:
- Summarize the dataset  
- Understand data distribution  
- Identify patterns and issues  

---

## Using `describe()` in Pandas

```python
df.describe()

Here are your notes, clean, structured, and ready to copy in **Markdown format**:

````md id="d7k2pl"
# Descriptive Statistics in EDA

## Why Descriptive Statistics?

Before building complex models, you should first **explore your data**.

Descriptive statistics help:
- Summarize the dataset  
- Understand data distribution  
- Identify patterns and issues  

---

## Using `describe()` in Pandas

```python
df.describe()
````

Returns statistics for numerical variables:

* count → number of values
* mean → average
* std → standard deviation
* min / max
* quartiles (25%, 50%, 75%)

Notes:

* Automatically skips missing values (NaN)
* Gives a quick overview of data distribution

---

## Categorical Data Analysis

Categorical variables:

* Represent groups or categories
* Example: drive system (FWD, RWD, 4WD)

### Using `value_counts()`

```python
df["column_name"].value_counts()
```

* Counts occurrences of each category
* Helps understand distribution of categories

---

## Box Plots

Box plots are used to visualize numerical data distribution.

### Key Components:

* Median → middle value
* 25th percentile → lower quartile
* 75th percentile → upper quartile
* IQR (Interquartile Range) → spread between Q1 and Q3
* Extremes → calculated using 1.5 × IQR
* Outliers → points outside extremes

### Why Use Box Plots?

* Detect outliers
* Understand distribution and skewness
* Compare groups

---

## Scatter Plots

Used to analyze relationships between two variables.

### Key Concepts:

* **Predictor variable (X)** → used to predict
* **Target variable (Y)** → value being predicted

Example:

* X → engine size
* Y → price

### In Python:

```python
plt.scatter(x, y)
```

* X-axis → predictor
* Y-axis → target

Always:

* Label axes
* Add a title

---

## Interpreting Scatter Plots

* Each point = one observation
* Helps identify relationships

Example insight:

* As engine size increases → price increases
* Indicates a **positive linear relationship**

---

## Key Insight

Descriptive statistics and visualizations help you:

* Understand data quickly
* Detect patterns and outliers
* Identify relationships between variables
* Prepare for further analysis

```
