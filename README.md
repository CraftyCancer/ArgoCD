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

**1. kubectl create namespace argocd**

**2. kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml**


Once the installtion is down, you will be able to see the pods running on our cluster on specified **namespace argocd**.

**3. kubectl get pods -n argocd**

![image](https://user-images.githubusercontent.com/113592437/221434779-632852c9-c9f0-4c4c-ad5b-aad0d323e28e.png)

**Note: Port Forward needs to be done to access the ArgoCD UI. **

**4. kubectl port-forward svc/argocd-server -n argocd 8092:443 ** 

(The port forward can be done through manifest file as well).

Try to access the ArgoCD UI by running the https://ip-adresss:8092 or (localhost) https://localhost:8092

![image](https://user-images.githubusercontent.com/113592437/221435255-4b8517b3-b33f-4b34-b479-ad2f6905b53a.png)

