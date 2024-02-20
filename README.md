### What is ArgoCD?


Argo CD is a declarative continuous delivery tool for Kubernetes. It can be used as a standalone tool or as a part of your CI/CD workflow to deliver needed resources to your clusters.

In order to manage infrastructure and application configurations aligned with GitOps, your Git repository must be the single source of truth. The desired state of your system should be versioned, expressed declaratively, and pulled automatically. This is where Argo CD comes in.

### How to setup ArgoCD on Mac M3?

1. Install Docker Desktop for Apple Silicon from [here](https://docs.docker.com/desktop/install/mac-install/).
2. Run Docker Desktop, click on the "Settings" button on top right and enable Kubernetes as depicted in the image below:

    <img src="dockerDesktopSettings.png" alt="Enable Kubernetes" width="600"/>
    <br />
    <br />

3. Then enter the commands below in your terminal for Non High Availability (Non HA) setup:

    ```
    minikube start

    kubectl create ns argocd

    kubectl apply -n argocd https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

    kubectl get pods -n argocd

    ```
    <br />

    The result of the commands should look like:

    <img src="commandResult.png" alt="Get Pods" width="600"/>
    <br />
    <br />

4. ArgoCD can be used now and one can start deploying applications.



### Resources
1. https://www.redhat.com/en/topics/devops/what-is-argocd