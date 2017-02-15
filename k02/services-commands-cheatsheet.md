# Create simple backend service and pod
```shell
kubectl create -f frontend-service-example.yaml
kubectl get pods,svc -o wide
kubectl describe svc/frontend-service
```

```
curl <hostname>:<port|nodePort if minikube>
Powered by Deis
```

# tail pod log file
```shell
kubectl logs po/<pod-name> -f
```

# Create external service and endpoint
# Not sure if this is possible w/minikube
```shell
kubectl create -f external-service-example.yaml
kubectl get svc
kubectl describe svc <svc-name>
```
