# Testing Strategies

**What it is:**
- Testing is the practice of validating software correctness, performance, and behavior before deployment.
- Effective testing improves reliability, catches regressions, and supports refactoring.

---

## Testing Levels

| Level         | Description |
|---------------|-------------|
| **Unit**      | Tests individual functions or methods in isolation |
| **Integration** | Tests multiple components working together (e.g., DB + service) |
| **End-to-End (E2E)** | Tests full application behavior from user perspective |
| **Smoke / Sanity** | Quick checks for critical paths |
| **Load / Performance** | Evaluates performance under stress or concurrency |

---

## Python Testing

- Use `pytest` for flexible unit/integration testing
- Fixtures for shared setup/teardown logic
- `mock` and `unittest.mock` for external dependency control

```python
import pytest
from myapp import add

def test_add():
    assert add(2, 3) == 5
```

- Run tests with:
```bash
pytest -v
pytest --maxfail=1 --disable-warnings
```

---

## Java Testing

- Use `JUnit 5` with annotations: `@Test`, `@BeforeEach`, `@AfterEach`
- Use `Mockito` or `EasyMock` for mocking
- Assertions via `assertEquals`, `assertThrows`, etc.

---

## Infrastructure Testing

| Tool          | Use Case |
|---------------|----------|
| `terratest`   | Test Terraform modules in Go |
| `kitchen-terraform` | Integration tests for IaC |
| `pytest` + `boto3` | Validate AWS resources exist or behave as expected |

---

## CI/CD Integration

- Run tests in GitHub Actions, Jenkins, or CircleCI
- Fail early on commit or PR
- Use code coverage tools (e.g., `coverage.py`, `jacoco`, Codecov)

---

## Best Practices
- Isolate unit tests from network, DB, filesystem
- Use test doubles (mocks/stubs/fakes) when needed
- Make tests fast and deterministic
- Prefer readable failure messages over clever logic

---

## Interview Tips
- Know when to mock vs. use test containers
- Explain your testing pyramid (more unit, fewer E2E)
- Be able to discuss test strategies in CI/CD
- Share how testing helped catch or prevent real-world bugs
