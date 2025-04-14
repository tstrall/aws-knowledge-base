# Scala

**What it is:**
- A hybrid functional + object-oriented programming language
- Runs on the JVM, interoperable with Java
- Widely used in data engineering (Spark), backend services, and streaming systems

---

## Core Features

- **Statically typed** with type inference
- **Immutability-first**: promotes safe concurrency and pure functions
- **Functional constructs**:
  - `map`, `flatMap`, `filter`, `reduce`
  - Higher-order functions, closures
- **Pattern matching**
- **Case classes** for lightweight data objects
- **Traits**: reusable units of behavior (like interfaces with mixins)

---

## Sample Code
```scala
case class Person(name: String, age: Int)

val people = List(
  Person("Alice", 30),
  Person("Bob", 25)
)

val adults = people.filter(_.age >= 18).map(_.name)
adults.foreach(println)
```

---

## Common Use Cases
- Spark jobs (RDD/DataFrame/DataSet APIs)
- Akka actors for concurrency
- Backend services (Play, http4s, Finagle)
- Kafka Streams or Flink with Scala APIs

---

## Scala in Apache Spark
- **Native API for Spark**
- More concise and performant than PySpark in complex jobs
- Supports both functional and SQL-style data transformations

---

## Tooling & Ecosystem
- **SBT**: Scala build tool
- **Ammonite**: interactive shell
- **Scalafmt**: formatter
- **Scalatest / MUnit**: testing libraries

---

## Interview Tips
- Be ready to talk about immutability, pattern matching, and higher-order functions
- Know how functional concepts help with Spark job safety and parallelism
- If using in Spark: know the differences between RDDs, DataFrames, and Datasets
