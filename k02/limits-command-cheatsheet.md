# Create limits namespace
```shell
kubectl create -f limits-namespace.yaml
```

# Apply limits to limits namespace
```shell
kubectl create -f limits-example.yaml
```

# Inspect limits
```shell
kubectl describe limits -n limits
```

# Run pod without resources defined verify defaults applied
```shell
kubectl run nginx --image=nginx --replicas=1 --namespace=limits
kubectl get po/nginx-701339712-9gpzj -n limits -o yaml | grep resources -C 8
```

# Run invalid pod
```shell
kubectl create -f limits-invalid-pod.yaml
```

# Run valid pod
```shell
kubectl create -f limits-valid-pod.yaml
```