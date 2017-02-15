# Create backend service and pod
```shell
kubectl create -f ingress-s1-example.yaml
kubectl create -f ingress-s2-example.yaml
kubectl get pods,svc,ep
```
# tail ingress-controller log file
```shell
kubectl logs po/<pod-name> -f
```

# Simple example
```shell
kubectl create -f ingress-simple-example.yaml
kubectl get ingress
kubectl describe ingress <ingress-name>
curl <hostname>
```

# Multi-path example
```shell
kubectl create -f ingress-multipath-example.yaml
curl http://<hostname>/<path-1>
curl http://<hostname>/<path-2>
```

# Multi-host example
```shell
kubectl create -f ingress-mutihost-example.yaml
curl http://<hostname-1>
curl http://<hostname-2>
```

# TLS example
```shell
kubectl create -f ingress-tls-secret.yaml
kubectl create -f ingress-tls-example.yaml
curl https://<hostname>
```
