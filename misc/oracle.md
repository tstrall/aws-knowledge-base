# Oracle Database

**What it is:**
- Enterprise-grade relational database management system (RDBMS) developed by Oracle Corporation
- Known for reliability, performance, and rich enterprise features

---

## Core Features

| Feature               | Description |
|-----------------------|-------------|
| **PL/SQL**            | Oracle's procedural SQL extension, supports packages, functions, triggers |
| **Tablespaces**       | Logical storage units mapped to physical storage |
| **Schemas / Users**   | Each user owns a schema (namespace of objects) |
| **Sequences**         | Used to generate unique numeric IDs |
| **Synonyms**          | Aliases for accessing objects (useful for abstraction) |
| **Materialized Views**| Cached query results that can be refreshed |
| **Partitioning**      | Improves query performance and manageability on large tables |

---

## Common Tasks

### Create Table
```sql
CREATE TABLE employees (
  id NUMBER PRIMARY KEY,
  name VARCHAR2(100),
  hire_date DATE
);
```

### Create Sequence
```sql
CREATE SEQUENCE emp_seq START WITH 1 INCREMENT BY 1;
```

### Use PL/SQL Block
```sql
BEGIN
  INSERT INTO employees (id, name) VALUES (emp_seq.NEXTVAL, 'Alice');
END;
/
```

---

## Performance & Tools
- **Explain Plan**: Analyze query execution strategy
- **AWR/ASH Reports**: Performance diagnostics and workload analysis
- **Oracle SQL Developer**: GUI client for database development
- **DBMS_STATS**: For collecting table/index stats to help optimizer

---

## Oracle in AWS
- Use **Amazon RDS for Oracle** (BYOL or License Included)
- Can migrate to **Aurora PostgreSQL** using **AWS DMS + SCT**
- Consider using Oracle for legacy apps and PostgreSQL for modernization

---

## Interview Tips
- Know PL/SQL basics: cursors, exception handling, packages
- Be ready to discuss migration strategies (e.g., Oracle → PostgreSQL)
- Understand indexing, partitioning, and optimizer stats
- Explain how to use synonyms, grants, and roles for secure schema access
