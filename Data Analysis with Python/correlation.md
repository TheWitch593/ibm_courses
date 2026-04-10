# Correlation in Data Analysis

## What Is Correlation?

Correlation is a statistical measure that shows:
- How two variables are related  
- How one variable changes when another changes  

---

## Key Idea

If one variable changes:
- Does the other increase?  
- Decrease?  
- Stay unrelated?  

---

## Important Note

**Correlation ≠ Causation**

- Just because two variables are related  
- Does NOT mean one causes the other  

Example:
- Rain and umbrellas → correlated  
- Umbrellas do NOT cause rain  

---

## Types of Correlation

### 1. Positive Correlation

- Both variables increase together  
- As one goes up → the other goes up  

Example:
- Engine size ↑ → Price ↑  

---

### 2. Negative Correlation

- One variable increases while the other decreases  

Example:
- Highway MPG ↑ → Price ↓  

---

### 3. Weak or No Correlation

- No clear relationship between variables  

Example:
- RPM vs Price → inconsistent pattern  

---

## Visualizing Correlation

### Scatter Plot

- Each point = one observation  
- Shows relationship between two variables  

---

### Regression Line

- A straight line added to the scatter plot  
- Shows overall trend  

- Steep slope → strong relationship  
- Flat slope → weak relationship  

---

## Examples

### Strong Positive Correlation
- Engine size vs Price  
- Larger engines → higher prices  

---

### Strong Negative Correlation
- Highway MPG vs Price  
- Better fuel efficiency → lower price  

---

### Weak Correlation
- Peak RPM vs Price  
- No clear pattern → poor predictor  

---

## Tools in Python

```python
sns.regplot(x="variable1", y="variable2", data=df)

Here are your notes, clean and ready to copy in **Markdown format**:

````md id="corr42x"
# Correlation in Data Analysis

## What Is Correlation?

Correlation is a statistical measure that shows:
- How two variables are related  
- How one variable changes when another changes  

---

## Key Idea

If one variable changes:
- Does the other increase?  
- Decrease?  
- Stay unrelated?  

---

## Important Note

**Correlation ≠ Causation**

- Just because two variables are related  
- Does NOT mean one causes the other  

Example:
- Rain and umbrellas → correlated  
- Umbrellas do NOT cause rain  

---

## Types of Correlation

### 1. Positive Correlation

- Both variables increase together  
- As one goes up → the other goes up  

Example:
- Engine size ↑ → Price ↑  

---

### 2. Negative Correlation

- One variable increases while the other decreases  

Example:
- Highway MPG ↑ → Price ↓  

---

### 3. Weak or No Correlation

- No clear relationship between variables  

Example:
- RPM vs Price → inconsistent pattern  

---

## Visualizing Correlation

### Scatter Plot

- Each point = one observation  
- Shows relationship between two variables  

---

### Regression Line

- A straight line added to the scatter plot  
- Shows overall trend  

- Steep slope → strong relationship  
- Flat slope → weak relationship  

---

## Examples

### Strong Positive Correlation
- Engine size vs Price  
- Larger engines → higher prices  

---

### Strong Negative Correlation
- Highway MPG vs Price  
- Better fuel efficiency → lower price  

---

### Weak Correlation
- Peak RPM vs Price  
- No clear pattern → poor predictor  

---

## Tools in Python

```python
sns.regplot(x="variable1", y="variable2", data=df)
````

* Creates scatter plot with regression line

---

## Key Insight

Correlation helps you:

* Identify relationships between variables
* Select important predictors
* Understand how variables influence each other

```
