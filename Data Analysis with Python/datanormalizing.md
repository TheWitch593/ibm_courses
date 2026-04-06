# Data Normalization in Pandas

## What Is Data Normalization?

Data normalization is a preprocessing technique used to make feature values **consistent in scale**.

Example:
- Length → 150 to 250  
- Width/Height → 50 to 100  

These different ranges can affect analysis.

---

## Why Normalization Is Important

Normalization helps:
- Make features comparable  
- Ensure equal impact of variables  
- Improve performance of models  
- Avoid bias caused by large-value features  

---

## Example Problem

Features:
- Age → 0 to 100  
- Income → 20,000 to 500,000  

Issue:
- Income values are much larger  
- Models (e.g., linear regression) will give more importance to income  
- This creates bias, even if income is not more important  

Solution:
- Normalize both features to similar ranges (e.g., 0 to 1)

---

## Normalization Methods

### 1. Simple Feature Scaling

Divide each value by the maximum value:
x_new = x / x_max


- Range → [0, 1]

Example in Python:

```python
df["length"] = df["length"] / df["length"].max()
2. Min-Max Normalization
x_new = (x - x_min) / (x_max - x_min)
Range → [0, 1]

Example in Python:

df["length"] = (df["length"] - df["length"].min()) / (df["length"].max() - df["length"].min())
3. Z-Score (Standardization)
x_new = (x - mean) / std
Mean → 0
Values typically between -3 and 3

Example in Python:

df["length"] = (df["length"] - df["length"].mean()) / df["length"].std()
Useful Pandas Methods
df.max() → maximum value
df.min() → minimum value
df.mean() → average
df.std() → standard deviation
Key Insight

Normalization ensures:

Fair comparison between features
Better model performance
Reduced bias from large-value variables