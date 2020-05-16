# portainer-k3s

If you want to install Portainer on Kubernetes, see the original project : https://github.com/portainer/portainer-k8s/

# Usage

## Deploy Portainer inside your cluster and access it via an external load balancer

```
kubectl apply -k overlays/<env>
```

## Update to a new version of the beta

In order to update to the latest version of the beta, you'll need to delete the `portainer-<env>` namespace and redeploy it.

```
kubectl delete namespace/portainer-<env>
kubectl apply -k overlays/<env>
```