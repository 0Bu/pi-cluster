# Kubernetes Dashboard
- [GitHub](https://github.com/kubernetes/dashboard)
- [k3s: Deploying the Kubernetes Dashboard](https://rancher.com/docs/k3s/latest/en/installation/kube-dashboard/)

## Helm repo
```
helm repo add kubernetes-dashboard https://kubernetes.github.io/dashboard/
helm repo update
```

## Helm values
`helm show values kubernetes-dashboard/kubernetes-dashboard > values.yaml`

## Helm install
`helm install -n kubernetes-dashboard --create-namespace dashboard kubernetes-dashboard/kubernetes-dashboard -f values.yaml`

## Helm uninstall
`helm uninstall -n kubernetes-dashboard dashboard`

## [K8S RBAC](https://rancher.com/docs/k3s/latest/en/installation/kube-dashboard/#dashboard-rbac-configuration)
`kubectl apply -f rbac.yaml`

## Auth token
`kubectl -n kubernetes-dashboard describe secret admin-user-token | grep '^token'`

