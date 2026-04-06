# Data Understanding in Pandas

Before starting any analysis, you should first understand the data.

Key things to check:
- Data types  
- Data distribution  
- Potential issues in the dataset  

---

## Why This Step Is Important

Exploring the dataset helps you:
- Detect incorrect data types  
- Identify inconsistencies or errors  
- Understand what operations can be applied  
- Spot issues like missing values or outliers  

---

## Data Types in Pandas

Common data types:

- object → used for strings or mixed data (can sometimes incorrectly store numbers as text)  
- int64 → integers (whole numbers)  
- float64 → decimal numbers  
- datetime64 / timedelta[ns] → date and time data (covered later)  

---

## Why Check Data Types

1. Type mismatches  
   Pandas assigns data types automatically, but it can be wrong.  
   Example: a numeric column stored as object instead of float.

2. Compatibility with operations  
   Some functions only work with numeric data.  
   Using them on the wrong type can cause errors.

---

## Checking Data Types

```python
df.dtypes