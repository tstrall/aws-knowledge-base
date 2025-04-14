# PostgreSQL

**What it is:**
- An advanced, open-source relational database known for extensibility, strong standards compliance, and rich feature set
- Supports both OLTP (transactional) and some OLAP (analytical) workloads

---

## Core Features

| Feature               | Description |
|-----------------------|-------------|
| **Schemas**           | Namespaces inside a database, used for logical separation |
| **Extensions**        | Add-ons like `postgis`, `uuid-ossp`, `pg_stat_statements` |
| **JSON/JSONB**        | Native support for semi-structured data |
| **CTEs**              | Common Table Expressions (`WITH` queries) for readable SQL |
| **Window Functions**  | Aggregate functions over partitions (e.g., `row_number()`) |
| **Foreign Data Wrappers (FDW)** | Query external sources like Oracle, MySQL, CSV |

---

## SQL Examples

### Create Table
```sql
CREATE TABLE users (
  id SERIAL PRIMARY KEY,
  email TEXT UNIQUE NOT NULL,
  created_at TIMESTAMPTZ DEFAULT now()
);
```

### JSON Query
```sql
SELECT data->>'name' FROM json_table WHERE data->>'type' = 'customer';
```

### CTE with Window Function
```sql
WITH ranked AS (
  SELECT *, ROW_NUMBER() OVER (PARTITION BY email ORDER BY created_at DESC) as rk
  FROM logins
)
SELECT * FROM ranked WHERE rk = 1;
```

---

## Performance Tools
- **`EXPLAIN` / `ANALYZE`**: Execution plan + runtime
- **`pg_stat_statements`**: Query tracking by frequency, time, etc.
- **Autovacuum**: Keeps table bloat under control
- **Partitioning**: Declarative in recent versions (by range/list/hash)
- **Parallel Queries**: Enabled by default since 9.6+

---

## Extensions to Know
- `pg_stat_statements`: Query performance stats
- `uuid-ossp`: Generates UUIDs
- `citext`: Case-insensitive text
- `timescaledb`: Time-series extension
- `postgis`: Geospatial support

---

## Interview Tips
- Be ready to talk about query tuning, indexes, and autovacuum
- Know how roles and grants work for schema access
- Understand the difference between `json` and `jsonb`
- Show off familiarity with `EXPLAIN ANALYZE` and `pg_stat_statements`
- Explain real-world experience with data types, constraints, and migrations
