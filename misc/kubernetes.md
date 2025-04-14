# Kubernetes (K8s)

**What it is:**
- Open-source platform for automating deployment, scaling, and management of containerized applications
- Originally developed by Google; now maintained by CNCF

---

## Core Concepts

| Concept         | Description |
|-----------------|-------------|
| **Pod**         | Smallest deployable unit, wraps one or more containers |
| **Deployment**  | Declarative update for Pods (rolling updates, replicas) |
| **Service**     | Stable networking endpoint (ClusterIP, NodePort, LoadBalancer) |
| **ConfigMap**   | External configuration (env vars, files) |
| **Secret**      | Encrypted config for sensitive data (API keys, passwords) |
| **Namespace**   | Logical cluster partitioning (e.g. dev, test, prod) |
| **Ingress**     | HTTP routing to Services (via path/host rules) |

---

## kubectl Cheatsheet

```bash
kubectl get pods
kubectl get services
kubectl describe pod <name>
kubectl logs <pod-name>
kubectl apply -f deployment.yaml
kubectl delete -f deployment.yaml
```

---

## Sample Deployment YAML
```yaml
apiVersion: apps/v1
kind: Deployment
metadata:
  name: my-app
spec:
  replicas: 3
  selector:
    matchLabels:
      app: my-app
  template:
    metadata:
      labels:
        app: my-app
    spec:
      containers:
      - name: app
        image: my-app:latest
        ports:
        - containerPort: 8080
```

---

## Common Tools & Add-ons

- **Helm** – Package manager for Kubernetes
- **Kustomize** – Native configuration customization
- **Prometheus/Grafana** – Monitoring stack
- **Argo CD** – GitOps deployment controller
- **Istio/Linkerd** – Service mesh for traffic control and security

---

## Interview Tips
- Explain how you scale an app in Kubernetes
- Discuss how to do zero-downtime deployments
- Know how config/secrets are managed
- Be ready to diagram Pods → Services → Ingress
