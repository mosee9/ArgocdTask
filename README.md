# ArgoCD Task for Tekton

This repository provides a reusable Tekton Task (`argocd-sync-and-wait`) that logs into ArgoCD, syncs a specified Application, and waits for it to reach Healthy + Synced status.

## Usage

1. Applied the secret and ConfigMap from `examples/`.
2. Applied the Task: `kubectl apply -f tasks/argocd-sync-and-wait.yaml`
3. Used it in the Pipeline or run directly via `tkn task start`.

Ideal for GitOps pipelines when we  need to trigger/promote deployments via ArgoCD.
