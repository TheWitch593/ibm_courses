# Grouping Data in Pandas

## What Is Grouping?

Grouping is a technique used to:
- Split data into subsets  
- Based on categories (categorical variables)  
- Analyze each group separately  

---

## Why Use Grouping?

Helps answer questions like:
- How does price vary by drive system?  
- Which category has the highest or lowest values?  

Example:
- Drive wheels → FWD, RWD, 4WD  
- Compare their average prices  

---

## Using `groupby()` in Pandas

```python
df.groupby("column_name")

Here are your notes, clean and ready to copy in **Markdown format**:

````md id="u9xw2k"
# Grouping Data in Pandas

## What Is Grouping?

Grouping is a technique used to:
- Split data into subsets  
- Based on categories (categorical variables)  
- Analyze each group separately  

---

## Why Use Grouping?

Helps answer questions like:
- How does price vary by drive system?  
- Which category has the highest or lowest values?  

Example:
- Drive wheels → FWD, RWD, 4WD  
- Compare their average prices  

---

## Using `groupby()` in Pandas

```python
df.groupby("column_name")
````

* Groups data by a categorical variable

---

## Example: Grouping Multiple Variables

```python
df_grouped = df[["drive-wheels", "body-style", "price"]]
df_grouped = df_grouped.groupby(["drive-wheels", "body-style"]).mean()
```

* Groups data by:

  * drive-wheels
  * body-style
* Calculates average price for each group

---

## Result

* Data is split into subcategories
* Shows mean price for each combination

Example insight:

* RWD convertibles and hardtops → highest prices
* 4WD hatchbacks → lowest prices

---

## Pivot Tables

Grouped data can be hard to read.

Use pivot tables to restructure data:

```python
df_pivot = df_grouped.pivot(index="drive-wheels", columns="body-style")
```

* Rows → one variable (e.g., drive-wheels)
* Columns → another variable (e.g., body-style)
* Values → aggregated data (e.g., mean price)

---

## Heatmaps

Heatmaps visualize pivot tables.

* Use color to represent values
* Easier to spot patterns

### Characteristics:

* Higher values → stronger/different colors
* Lower values → lighter colors

---

## Why Use Heatmaps?

* Visualize relationships between variables
* Quickly identify trends and patterns
* Compare multiple variables at once

---

## Key Insight

Grouping and visualization help you:

* Break down complex data
* Compare categories easily
* Discover relationships between variables and target

```
