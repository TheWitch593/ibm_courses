# Handling Missing Values in Pandas

## What Are Missing Values?

A missing value occurs when no data is stored for a feature in a specific observation.

Common representations:
- NaN (Not a Number)
- NA
- ?
- 0 (sometimes)
- Empty/blank cells

---

## Why Missing Data Matters

Missing values can:
- Affect analysis accuracy  
- Cause errors in calculations  
- Lead to incorrect conclusions  

---

## Ways to Handle Missing Values

### 1. Get the Missing Data
- Ask the data source to provide the correct values  
- Best option when possible  

---

### 2. Remove Missing Data

You can:
- Drop entire rows (observations)
- Drop entire columns (features)

Guidelines:
- If only a few rows are missing → drop rows  
- If many values are missing in a column → consider dropping the column  
- Always try to minimize data loss  

---

### 3. Replace Missing Data (Imputation)

Instead of deleting, you can replace missing values.

Common methods:

- **Mean (average)** → for numerical data  
- **Mode (most frequent value)** → for categorical data  
- **Custom values** → based on domain knowledge  

Example:
- If a column average is 4500 → replace missing values with 4500  

---

### 4. Leave Missing Data As Is

Sometimes keeping missing values is useful, depending on the analysis.

---

## Handling Missing Data in Pandas

### Dropping Missing Values

```python
df.dropna()

Options:

axis=0 → drop rows with missing values
axis=1 → drop columns with missing values
inplace=True → apply changes directly to the dataset

Example:

df.dropna(axis=0, inplace=True)
Replacing Missing Values
df.replace()

Example (replace NaN with mean):

mean_value = df["column_name"].mean()
df["column_name"].replace(np.nan, mean_value, inplace=True)
Important Notes
inplace=True modifies the dataset directly
Without inplace=True, the original DataFrame is not changed
Always check documentation if unsure
Key Insight

There is no single correct way to handle missing data.

You should:

Understand the dataset
Choose the method with the least negative impact
Balance accuracy vs data loss