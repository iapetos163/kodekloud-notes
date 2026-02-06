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