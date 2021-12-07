# Longhorn
- [Longhorn](https://longhorn.io)

# [Installtion requirements](https://longhorn.io/docs/1.2.2/deploy/install/#installation-requirements)
```
sudo apt install open-iscsi -y

```

## [Helm install](https://longhorn.io/docs/1.2.2/deploy/install/install-with-helm/)
```
helm repo add longhorn https://charts.longhorn.io
helm repo update
helm install longhorn longhorn/longhorn --namespace longhorn-system --create-namespace
```

## [Helm unintall](https://longhorn.io/docs/1.2.2/deploy/uninstall/#uninstalling-longhorn-using-helm)
```
helm uninstall longhorn -n longhorn-system
``` 
