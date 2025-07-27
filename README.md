# dev-argocd-consul

This repository contains ArgoCD application manifests for deploying HashiCorp Consul to a Kubernetes cluster.

## Structure

```
dev-argocd-consul/
├── consul/
│   └── application.yaml    # ArgoCD Application manifest for Consul deployment
```

## Description

The repository is configured to deploy Consul using ArgoCD, with the following features:

- Deploys Consul from the official HashiCorp Helm chart
- Configures a single-server deployment for development purposes
- Enables the Consul UI
- Enables Connect Inject for service mesh capabilities
- Implements automated sync with pruning and self-healing
- Creates the required namespace automatically

## Usage

1. Make sure you have ArgoCD installed in your Kubernetes cluster
2. Apply the application manifest:
   ```bash
   kubectl apply -f consul/application.yaml
   ```
3. ArgoCD will automatically sync and deploy Consul to your cluster
