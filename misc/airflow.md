# Apache Airflow

**What it is:**
- A platform to programmatically author, schedule, and monitor workflows
- Uses Directed Acyclic Graphs (DAGs) to manage task dependencies
- Written in Python; highly extensible with custom operators and plugins

---

## Core Concepts

| Concept      | Description |
|--------------|-------------|
| **DAG**      | Directed Acyclic Graph defining workflow structure |
| **Task**     | A unit of work in the DAG (defined using an Operator) |
| **Operator** | Defines what to do (e.g. BashOperator, PythonOperator, PostgresOperator) |
| **Scheduler**| Picks up DAGs and triggers task execution at the defined intervals |
| **Executor** | Manages how tasks run (Local, Celery, Kubernetes, etc.) |
| **XCom**     | Mechanism for sharing data between tasks |
| **Hook**     | Interface to external systems (S3, DBs, APIs) |

---

## Sample DAG (Python)
```python
from airflow import DAG
from airflow.operators.bash import BashOperator
from datetime import datetime

default_args = {
    'start_date': datetime(2024, 1, 1),
    'retries': 1,
}

dag = DAG(
    'example_dag',
    schedule_interval='@daily',
    default_args=default_args,
    catchup=False,
)

t1 = BashOperator(
    task_id='print_date',
    bash_command='date',
    dag=dag
)

t2 = BashOperator(
    task_id='say_hello',
    bash_command='echo Hello World',
    dag=dag
)

t1 >> t2  # Task dependencies
```

---

## Common Use Cases
- ETL pipelines
- ML workflows (training, batch inference)
- Data quality checks
- Reporting and dashboard refreshes

---

## Scheduling Basics
- `@hourly`, `@daily`, `@weekly`, or cron-style: `0 8 * * 1`
- `catchup=False`: Don’t backfill missed intervals

---

## Deployment
- Standalone: LocalExecutor
- Distributed: CeleryExecutor, KubernetesExecutor
- Hosted: MWAA (Amazon Managed Workflows for Apache Airflow), Astronomer, Google Cloud Composer

---

## Interview Tips
- Know how Airflow differs from tools like Luigi or Prefect
- Be able to explain how retries, failure alerts, and backfilling work
- Understand task isolation, scheduling delays, and DAG versioning

