# Java

**What it is:**
- A high-level, object-oriented programming language
- Known for portability (Write Once, Run Anywhere), strong typing, and vast ecosystem
- Widely used for backend systems, big data platforms, and Android development

---

## Core Concepts

- **Classes & Objects**: Everything is wrapped in a class
- **Static typing**: All variables must be declared with a type
- **Inheritance & Interfaces**: Supports polymorphism and abstraction
- **Exception Handling**: Try/catch/finally model
- **JVM (Java Virtual Machine)**: Platform for executing bytecode

---

## Sample Code
```java
public class HelloWorld {
    public static void main(String[] args) {
        System.out.println("Hello, World!");
    }
}
```

---

## Common Keywords
- `public`, `private`, `protected`
- `static`, `final`, `abstract`
- `implements`, `extends`
- `try`, `catch`, `finally`, `throw`, `throws`

---

## Collections Overview

| Type         | Description                        |
|--------------|------------------------------------|
| `List`       | Ordered collection (e.g., ArrayList) |
| `Set`        | Unordered unique collection         |
| `Map`        | Key-value pairs (e.g., HashMap)     |
| `Queue`      | FIFO structure                      |

---

## Java in Big Data / Backend
- Apache Spark and Hadoop often use Java or Scala APIs
- Kafka clients and connectors written in Java
- Spring Boot for web APIs and microservices

---

## Tooling & Ecosystem
- **Build tools**: Maven, Gradle
- **IDE**: IntelliJ IDEA, Eclipse
- **Testing**: JUnit, Mockito
- **Frameworks**: Spring, Hibernate, Vert.x

---

## Java 17+ Features

| Version | Feature                              | Description |
|---------|---------------------------------------|-------------|
| 14      | **Records**                           | Concise data carriers (`record Person(String name, int age)`) |
| 15+     | **Text Blocks**                       | Multi-line string literals using `"""` |
| 16      | **Pattern Matching (instanceof)**     | Simplifies casting after type checks |
| 17      | **Sealed Classes**                    | Restrict which classes can extend a superclass |
| 17      | **Switch Expressions (preview earlier)** | More concise and functional switch syntax |
| 17      | **Enhanced Pseudo-Random Generators** | Improved and flexible random number APIs |
| 18-21   | **Continued pattern matching, virtual threads (preview), structured concurrency** | Ongoing modernization of concurrency and data modeling |

---

## Interview Tips
- Understand memory management and garbage collection
- Know the difference between `==` and `.equals()`
- Practice with collection manipulation and sorting
- Be able to discuss multithreading (`Runnable`, `synchronized`, `ExecutorService`)
- Be familiar with modern language features like records, pattern matching, and virtual threads

Let me know if you'd like additions on streams, lambdas, or concurrency enhancements in Java 21+!

