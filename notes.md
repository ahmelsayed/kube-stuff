```bash
# create a cluster
az aks create -g {resourceGroup} -n {clusterName}

# get cluster kubectl
az aks get-credentials --resource-group {resourceGroup} --name {clusterName}

# apply
kubectl apply -f fileName.yaml

# get resources
kubectl get pods # <name> -o yaml
kubectl get deployments
kubectl get services



# run a shell in cluster
kubectl run -i --tty curl-shell --image=tutum/curl --restart=Never -- bash
```