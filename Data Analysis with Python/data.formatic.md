# Data Formatting in Pandas

## What Is Data Formatting?

Data formatting means converting data into a **common standard format** so it can be:
- Easily understood  
- Consistent  
- Ready for analysis  

---

## Why Data Formatting Is Important

Data is often:
- Collected from different sources  
- Stored in different formats  
- Written using different conventions  

Example:
- "New York", "NY", "N.Y." → same meaning, different formats  

Without formatting:
- Analysis becomes difficult  
- Comparisons are inaccurate  

---

## When Inconsistent Data Can Be Useful

Sometimes, different formats are helpful:
- Detecting patterns in how people write data  
- Identifying anomalies or fraud  

But most of the time:
- We standardize data for easier analysis  

---

## Example: Unit Conversion

Dataset may contain different measurement systems.

Example:
- Fuel consumption in **miles per gallon (mpg)**  
- Convert to **liters per 100 km (L/100km)**  

Formula:
L/100km = 235 / mpg


In Python:

```python
df["city_L/100km"] = 235 / df["city_mpg"]

Rename column:

df.rename(columns={"city_mpg": "city_L/100km"}, inplace=True)
Data Type Issues

Sometimes data types are incorrect after importing.

Example:

"price" stored as object instead of int or float

Problems:

Models may behave incorrectly
Valid data may be treated as missing
Common Data Types in Pandas
object → strings (text)
int64 → integers
float64 → decimal numbers
Checking Data Types
df.dtypes
Shows the data type of each column
Converting Data Types

Use astype() to change types:

df["price"] = df["price"].astype("int")
Converts column to integer type
Key Insight

Data formatting ensures:

Consistency across the dataset
Correct data types
Reliable analysis and modeling