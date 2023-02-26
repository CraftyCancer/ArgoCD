# Argo CD

## What is Argo CD?
Argo CD is a declarative, GitOps continuous delivery tool for Kubernetes.

## Why Argo CD?
- Application definitions, configurations, and environments should be declarative, and version controlled. Application deployment and lifecycle management should be automated, auditable, and easy to understand.

- Argo CD automates the deployment of the desired application states in the specified target environments. Application deployments can track updates to branches, tags, or pinned to a specific version of manifests at a Git commit.

- It monitors your cluster and your declaratively-defined infrastructure stored in a Git repository and resolves differences between the two — effectively automating an application deployment. 

## Installtion

Installtion of Argo CD is straight forward, we use the below raw-manifest provided by Argo CD and deploy on our kuberenetes cluster.

### Run the below command

- Run the below command on your exisiting kubernetes cluster.

**kubectl create namespace argocd**
**kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml**


