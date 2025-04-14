# Argo Workflows & Argo CD

**What it is:**
- **Argo Workflows**: A Kubernetes-native workflow engine for running DAGs of jobs
- **Argo CD**: A declarative GitOps tool for continuous delivery on Kubernetes
- Part of the Argo Project ecosystem (with Argo Events and Rollouts)

---

## Argo Workflows

### Core Concepts
| Concept        | Description |
|----------------|-------------|
| **Workflow**   | Custom resource (CRD) that defines a DAG of tasks |
| **Template**   | A reusable step or container to run in a pod |
| **Steps**      | Sequential or parallel actions within the workflow |
| **Artifacts**  | Files passed between steps |
| **Parameters** | Input values for workflow templates |

### Sample Workflow YAML
```yaml
apiVersion: argoproj.io/v1alpha1
kind: Workflow
metadata:
  generateName: hello-world-
spec:
  entrypoint: whalesay
  templates:
    - name: whalesay
      container:
        image: docker/whalesay
        command: [cowsay]
        args: ["hello world"]
```

---

## Argo CD

### Core Concepts
| Concept     | Description |
|-------------|-------------|
| **Application** | CRD that syncs a Git repo to a Kubernetes namespace |
| **Sync**        | Applies manifests from Git to the cluster |
| **Health**      | Status evaluation (Healthy/Degraded) |
| **Hooks**       | Pre/post sync job execution |

### Argo CD Features
- Automatically detects and syncs changes from Git
- UI and CLI support
- RBAC, SSO, and audit logs
- Supports Kustomize, Helm, and plain YAML

---

## Use Cases
- Run multi-step ML training or ETL pipelines (Workflows)
- Implement GitOps CD for microservices (Argo CD)
- Replace Jenkins for Kubernetes-native automation

---

## Tooling & Ecosystem
- `argocd` CLI: manage apps from terminal
- Argo UI: visualize workflows and sync state
- Argo Events: Event-based triggers (e.g., S3, Git, Webhook)
- Argo Rollouts: Progressive delivery (blue/green, canary)

---

## Interview Tips
- Know the GitOps model: Git as source of truth, pull-based deployment
- Describe how Argo CD compares to Flux, Jenkins X, Spinnaker
- Show how Argo Workflows replaces DAG-based Airflow jobs for K8s-native stacks
- Mention CRDs and how Argo integrates cleanly into Kubernetes
