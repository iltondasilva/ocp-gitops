# ocp-gitops

Desired state for the OpenShift cluster `ocp.capsulesensor.com` (4.22, Agent-based Installer, bare-metal profile, 3-node compact).
Argo CD (Red Hat OpenShift GitOps) watches this repo and keeps the cluster matching it. Changes arrive by pull request.

- `apps/webapp-demo/` - the httpd demo application: Namespace, Deployment (3 replicas, probes, pinned image), Service, Route.
- `argocd/` - the Argo CD Application definitions (automated sync, prune, selfHeal).
