# Taints & Tolerations

```sh
# Do not place pods on the node unless the pod tolerates the taint k/v pair
kubectl taint nodes mynode arbitrarykey=arbitraryvalue:NoSchedule
# Also: PreferNoSchedule
# NoExecute - kick out intolerant pods
```

Taints are how the master node prevents pods from running on it by default

```sh
kubectl describe node kubemaster | grep Taint
```

Remove a taint:

```sh
kubectl taint nodes <node-name> <key>-
```

# Node Selectors

Label nodes for usage with node selectors

```sh
kubectl label node <node-name> key=value
```
