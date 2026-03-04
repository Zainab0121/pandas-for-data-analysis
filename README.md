# 🐼 PANDAS_101 — Pandas Data Analysis Study Notes

A practical, example-driven Jupyter Notebook covering data manipulation and analysis using the Pandas library. Written as personal study notes with annotated code examples using a real-world dataset (Titanic).

---

##  Topics Covered

| # | Topic | Key Functions / Methods |
|---|-------|------------------------|
| 1 | **What is Pandas?** | Series, DataFrame overview |
| 2 | **Loading Data** | `pd.read_csv()` |
| 3 | **DataFrame Basics** | `head()`, `tail()`, `info()`, `describe()`, `dtypes`, `columns`, `shape` |
| 4 | **Selecting & Indexing** | `df[]`, `df[[]]`, `.loc[]`, `.iloc[]` |
| 5 | **Boolean Indexing** | Filtering rows with conditions |
| 6 | **Sorting** | `sort_values()` |
| 7 | **New Columns** | Direct assignment, `.assign()`, `.insert()` |
| 8 | **Missing Data** | `isnull()`, `isna()`, `dropna()`, `fillna()` |
| 9 | **Mean / Median / Mode** | Imputation strategies explained |
| 10 | **GroupBy Operations** | `groupby()`, `agg()`, `transform()`, `apply()` |

---

##  Dataset

The notebook uses the **Titanic dataset** (`train.csv`) as the working example throughout.

To use your own dataset, update the file path in the data-loading cell:

```python
# Replace this path with your own CSV file
df = pd.read_csv("path/to/your/file.csv")
```

You can download the Titanic dataset from [Kaggle](https://www.kaggle.com/datasets/hesh97/titanicdataset-traincsv) or use any CSV of your choice.

---

##  Key Concepts at a Glance

### `.loc` vs `.iloc`
| Method | Based on | Example |
|--------|----------|---------|
| `.loc` | Labels / index names | `df.loc[2, 'Name']` |
| `.iloc` | Integer positions | `df.iloc[0, 1]` |

### `agg` vs `transform` vs `apply`
| Method | Returns | Best for |
|--------|---------|---------|
| `agg()` | One result per group | Summary tables, reports |
| `transform()` | Same shape as original | Adding new columns, normalization |
| `apply()` | Custom output | Complex/custom logic per group |

### Missing Data Imputation
| Strategy | Use when |
|----------|---------|
| **Mean** | Numeric data, normal distribution |
| **Median** | Numeric data with skew or outliers |
| **Mode** | Categorical data |

---

##  How to Run

### Requirements
- Python 3.x
- Pandas
- Jupyter Notebook or JupyterLab

```bash
pip install pandas jupyter
jupyter notebook PANDAS_101.ipynb
```

### Tips
- Run cells **top to bottom** — some cells depend on earlier ones.
- Update the CSV file path in the loading cell before running.
- Experiment with the examples using your own datasets!

---

##  Notes

- This notebook is written as **personal study notes** — explanations are in plain, beginner-friendly language.
- Code cells include comments explaining what each line does.
- The notebook is self-contained and covers the most commonly used Pandas operations for data analysis.
