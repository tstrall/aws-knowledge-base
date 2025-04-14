# Pandas (Python Data Analysis Library)

**What it is:**
- Powerful Python library for data manipulation and analysis
- Built on top of NumPy; integrates well with Jupyter, matplotlib, scikit-learn, etc.

---

## Core Concepts

- **Series:** 1D labeled array (like a column)
- **DataFrame:** 2D labeled table (rows + columns)

```python
import pandas as pd

df = pd.read_csv("data.csv")
```

---

## Common Operations

```python
# View data
print(df.head())
df.info()
df.describe()

# Select columns
ages = df["age"]
subset = df[["name", "age"]]

# Filtering
adults = df[df["age"] >= 18]

# New columns
df["age_squared"] = df["age"] ** 2

# Grouping and aggregation
df.groupby("country")["income"].mean()

# Sorting
df.sort_values("age", ascending=False)

# Missing data
df.dropna()
df.fillna(0)
```

---

## Writing Data
```python
df.to_csv("cleaned.csv", index=False)
df.to_parquet("data.parquet")
```

---

## Pandas + PyFlink
- Use pandas for pre-processing or post-analysis in Flink jobs
- Can convert between PyFlink Table and pandas DataFrame using `to_pandas()` or `from_pandas()`

```python
pandas_df = flink_table.to_pandas()
flink_table = t_env.from_pandas(pandas_df)
```

---

## Tips
- Use `astype()` to convert column types
- Vectorized operations are faster than `apply()`
- Use `.query()` for readable filtering
