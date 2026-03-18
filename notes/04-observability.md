A pod has a STATUS (enum) e.g. Pending, Running
It also has CONDITIONS (booleans) that are tied to the pod lifecycle. "Ready" is one such condition

`readinessProbe` lets us assert our own condition to judge a container as ready

PROTIP: add the `-w` flag to kubectl commands to watch status
