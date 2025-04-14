# GitHub Actions (CI/CD)

**What it is:**
- Native automation platform for GitHub repos
- Used for CI/CD pipelines, Terraform deployments, testing, Docker builds, etc.

**Core Concepts:**
- **Workflow:** YAML file in `.github/workflows/`
- **Trigger events:** `push`, `pull_request`, `schedule`, `workflow_dispatch`
- **Jobs & Steps:** Parallel/serial units of work
- **Runners:** Hosted or self-hosted execution environments
- **Secrets:** Stored in repo/org and referenced via `${{ secrets.MY_SECRET }}`

**Key Syntax:**
```yaml
name: CI Pipeline
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
      - name: Run tests
        run: pytest
```

**Use Cases to Know:**
- Lint/test on PR
- Terraform `plan` & `apply`
- Deploy serverless apps or containers
