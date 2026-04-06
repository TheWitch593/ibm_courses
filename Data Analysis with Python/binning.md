# Data Binning in Pandas

## What Is Binning?

Binning is a data preprocessing technique where we **group continuous values into categories (bins)**.

Example:
- Age → 0–5, 6–10, 11–15  

---

## Why Use Binning?

Binning helps:
- Simplify data  
- Improve model accuracy (in some cases)  
- Better understand data distribution  
- Convert numerical data into categorical data  

---

## Example: Price Binning

- Original data:  
  - Price range → 5,000 to 45,500  
  - Many unique values  

- After binning:
  - Low price  
  - Medium price  
  - High price  

This reduces complexity and makes patterns easier to see.

---

## Creating Bins in Python

### Step 1: Create Bin Intervals

Use NumPy to create evenly spaced bins:

```python
bins = np.linspace(min_value, max_value, number_of_bins + 1)

Example:

bins = np.linspace(df["price"].min(), df["price"].max(), 4)
Step 2: Create Labels
group_names = ["Low", "Medium", "High"]
Step 3: Apply Binning

Use pandas cut():

df["price_binned"] = pd.cut(df["price"], bins, labels=group_names, include_lowest=True)
Visualizing Binned Data

Use a histogram to see distribution:

Shows how many values fall into each bin
Helps identify patterns

Example insight:

Most cars → low price
Few cars → high price
Key Insight

Binning:

Reduces number of unique values
Makes data easier to interpret
Helps reveal trends in the dataset
