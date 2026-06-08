# Test Kubernetes deployments with minikube


## Installation

1. Install minikube (4CPU + 8GB for istio)
2. Enable istio plugins
3. Install argocd [Tutorial](https://medium.com/@mehmetodabashi/installing-argocd-on-minikube-and-deploying-a-test-application-caa68ec55fbf)
4. Install rollout CRDS [Quick Start](https://argo-rollouts.readthedocs.io/en/stable/)
5. Install [kubectl plugin](https://argo-rollouts.readthedocs.io/en/stable/installation/)
6. 


Start minikube
```bash
minikube start
minikube tunnel
```

Port forwar to argoCD deployment to open [argoCD Web front](https://127.0.0.1:8080)
```bash
kubectl port-forward svc/argocd-server -n argocd 8080:443
```

Start dashboard and open [ArgoCD Rollout dashboard](http://127.0.0.1:3100)
```bash
kubectl argo rollouts dashboard
```