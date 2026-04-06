# Converting Categorical Variables to Numerical (Encoding)

## Why Convert Categorical Data?

Most statistical and machine learning models:
- Cannot work with strings (text)  
- Require numerical input  

Example:
- Fuel type → "gas", "diesel" (categorical)  
- Must be converted into numbers  

---

## One-Hot Encoding

One-hot encoding is a technique used to convert categorical variables into numeric form.

### How It Works

For each unique category:
- Create a new column (feature)  
- Use:
  - `1` → if the category is present  
  - `0` → if not  

---

### Example

Original column:

| Fuel |
|------|
| Gas  |
| Diesel |

After encoding:

| Gas | Diesel |
|-----|--------|
| 1   | 0      |
| 0   | 1      |

---

## Using Pandas

Pandas provides a built-in method:

```python
pd.get_dummies()

Example:

df_dummies = pd.get_dummies(df["fuel"])
Automatically creates new columns for each category
Assigns 1s and 0s accordingly
Key Insight

One-hot encoding:

Transforms categorical data into numerical format
Makes data usable for models
Preserves category information without ranking them