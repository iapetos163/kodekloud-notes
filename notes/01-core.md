# Useful commands / args

```sh
kubectl get pod -o yaml > pod-definition.yaml

# test a command
--dry-run=client

# This command will let you generate a template from scratch!
kubectl run nginx --image=nginx --dry-run=client -o yaml

# List the available resource kinds
kubectl api-resources

# Get documentation on available args
kubectl explain pods

# Use dot notation to dig into nested fields
kubectl explain pods.spec

# List all available fields
kubectl explain pods --recursive
```

https://kubernetes.io/docs/reference/kubectl/quick-reference/

# Accessing resource in another namespace

```
my-service.other-namespace.svc.cluster.local
```

```
kubectl create namespace
```

# Services

objects for network config

- NodePort - map a port on the node to a port on the pod
- ClusterIP
- LoadBalancer

port terminology from the perspective of the _service_
Port: port of the service
TargetPort: port of pod
NodePort: port on the node
