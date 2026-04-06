
## Importing Data in Python

Importing data means loading data into Python so you can analyze or process it.

Two important properties when working with data:

* **Format** – the type of file (e.g., `.csv`, `.json`, `.xlsx`)
* **File path** – where the file is located

Examples of file paths:

* On your computer: `/desktop/mydata.csv`
* From the internet: a URL link

---

## How to Import a File

First, you need to import the required library:

```python
import pandas as pd
```

Then define the path:

```python
url = "your_link_here"
path = "your_file_path_here"
```

Read the file using pandas:

```python
df = pd.read_csv(url)
```

If the dataset does not have column headers:

```python
df = pd.read_csv(url, header=None)
```

---

## Viewing the Data

* `df` → displays the entire dataset (not recommended for large datasets)
* `df.head(n)` → shows the first *n* rows
* `df.tail(n)` → shows the last *n* rows

---

## Adding or Modifying Headers

To make the dataset easier to work with, you can rename the columns:

```python
df.columns = headers
```

Steps:

1. Create a list of column names
2. Assign it to `df.columns`
3. Check the result using `df.head()`

---

## Exporting Data

You can save your processed data to a file:

```python
path = "your_output_path_here"
df.to_csv(path)
```

This is useful for saving progress or results.

---

## Working with Different File Formats

Pandas supports multiple file formats:

 **CSV**

  ```python
  pd.read_csv()
  df.to_csv()
  ```

 **JSON**

  ```python
  pd.read_json()
  df.to_json()
  ```

 **Excel**

  ```python
  pd.read_excel()
  df.to_excel()
  ```

 **SQL**
  (used with databases, requires a connection)

