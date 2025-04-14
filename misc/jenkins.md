# Jenkins (CI/CD)

**What it is:**
- An open-source automation server used for building, testing, and deploying code
- Highly extensible with plugins; often used in traditional CI/CD pipelines

---

## Key Concepts

| Concept     | Description |
|-------------|-------------|
| **Job**     | A unit of work to be executed (Freestyle or Pipeline) |
| **Pipeline**| Code-defined CI/CD flow using `Jenkinsfile` syntax |
| **Node/Agent** | Worker machine that runs jobs (can be Docker, EC2, etc.) |
| **Executor**| Thread on a node used to run one job at a time |
| **Plugin**  | Modular extension (e.g., Git, Slack, Docker, Artifactory) |

---

## Jenkinsfile Example
```groovy
pipeline {
  agent any
  stages {
    stage('Build') {
      steps {
        sh 'npm install'
      }
    }
    stage('Test') {
      steps {
        sh 'npm test'
      }
    }
    stage('Deploy') {
      steps {
        sh './deploy.sh'
      }
    }
  }
}
```

---

## Installation Options
- `.war` file (Java-based)
- Docker container (`jenkins/jenkins:lts`)
- Helm chart for Kubernetes
- AWS EC2 AMI or Jenkins controller + agents pattern

---

## Common Plugins
- Git / GitHub integration
- Slack notifications
- Pipeline steps (UI + DSL)
- Credentials Binding
- AWS CLI / S3 / CodeDeploy
- Docker Pipeline

---

## Declarative vs Scripted Pipelines
- **Declarative**: Structured, safer, easier to read (recommended)
- **Scripted**: Groovy-based, more flexible but harder to maintain

---

## Tips for Team Use
- Store Jenkinsfile in repo (GitOps pattern)
- Use credentials binding to inject secrets securely
- Run test suites in parallel
- Archive artifacts (logs, builds) for post-job access

---

## Interview Tips
- Know Jenkinsfile syntax and pipeline stages
- Explain controller/agent setup and scaling
- Describe integration with Git, Docker, or cloud services
- Highlight use of shared libraries and job templating
