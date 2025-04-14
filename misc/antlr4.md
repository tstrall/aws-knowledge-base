# ANTLR 4 (Another Tool for Language Recognition)

**What it is:**
- A powerful parser generator used to read, process, translate, or execute structured text or binary files
- Commonly used for building compilers, interpreters, DSLs, and config readers

---

## Core Concepts

| Concept     | Description |
|-------------|-------------|
| **Grammar** | Defines the syntax rules for a language (written in `.g4` files) |
| **Lexer**   | Tokenizes the input (e.g., numbers, keywords) |
| **Parser**  | Builds a parse tree using the grammar rules |
| **Listener**| Auto-generated visitor with entry/exit hooks for each grammar rule |
| **Visitor** | Custom traversal strategy, like a manual walk through the tree |

---

## Basic Grammar Example
```antlr
grammar Hello;

r : 'hello' ID ;
ID : [a-zA-Z]+ ;
WS : [ \t\r\n]+ -> skip ;
```

---

## How to Use (Java Example)
```bash
antlr4 Hello.g4         # generate lexer + parser
javac Hello*.java       # compile
grun Hello r -tokens    # test rule 'r' on input
```

In code:
```java
HelloLexer lexer = new HelloLexer(CharStreams.fromString("hello world"));
HelloParser parser = new HelloParser(new CommonTokenStream(lexer));
parser.r();
```

---

## Common Use Cases
- DSLs (Domain Specific Languages)
- SQL-like interpreters
- Language transpilers (e.g., DSL → Python)
- Code analysis / linters / query validators

---

## Tips & Gotchas
- Rule names starting with lowercase = parser rules, uppercase = lexer rules
- Left-recursion is supported in ANTLR 4 (unlike many other tools)
- Use `-visitor` flag to generate visitor pattern classes
- `grun` helps with grammar debugging (lookahead, tokens, trees)

---

## Interview Tips
- Know how parsing differs from tokenization
- Be able to explain listener vs visitor patterns
- Know when to use ANTLR vs regex or hand-written parsers
- Useful to highlight if you've built interpreters, linters, or migrations tools
