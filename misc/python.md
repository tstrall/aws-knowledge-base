# Python

**What it is:**
- A high-level, interpreted, general-purpose programming language
- Known for simplicity, readability, and vast ecosystem

---

## Core Concepts

- **Dynamic typing** and **duck typing**
- **Indentation-based syntax**
- **First-class functions** and **closures**
- Supports **OOP**, **functional**, and **imperative** styles
- Extensive standard library (`os`, `json`, `datetime`, `re`, `math`, etc.)

---

## Common Syntax
```python
def greet(name):
    return f"Hello, {name}!"

names = ["Alice", "Bob", "Carol"]
for n in names:
    print(greet(n))
```

---

## Data Structures

| Type       | Description |
|------------|-------------|
| `list`     | Ordered, mutable, allows duplicates |
| `tuple`    | Ordered, immutable |
| `set`      | Unordered, unique elements |
| `dict`     | Key-value pairs |

---

## Libraries to Know (by Domain)

- **Data**: `pandas`, `numpy`, `polars`
- **Visualization**: `matplotlib`, `seaborn`, `plotly`
- **Machine Learning**: `scikit-learn`, `xgboost`, `tensorflow`, `pytorch`
- **Web**: `flask`, `fastapi`, `django`
- **ETL / Infra**: `boto3`, `sqlalchemy`, `airflow`, `requests`, `click`

---

## Virtual Environments
```bash
python3 -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

---

## Tips for Interviews
- Use list comprehensions over `map`/`filter` where possible
- Know how to write idiomatic Python using `with`, `enumerate`, `zip`
- Be prepared to reverse strings, deduplicate lists, parse JSON, etc.
- Mention experience with packaging, testing (`pytest`), linting (`flake8`, `black`)
