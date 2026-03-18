Edit a deployment in-place (and therefore its pods)

```sh
kubectl edit deployment my-deployment
```

# Secrets

Create a secret imperative command

```sh
# may repeat --from-literal for multiple k/v pairs
kubectl create secret generic mysecret --from-literal key=value
```

# Admin: encryption

```sh
# Check the API server's encryption
ps aux | grep kube-api | grep --encryption-provider-config
```

# IAM: Service accounts

```sh
kubectl get serviceacount

# default: 1h
kubectl create token my-sa --duration 2h
```
