# minikube
```shell
minikube start
minikube addons list
minikube service list
minikube dashboard
```

# config
```shell
cat ~/.kube/config
kubectl config get-contexts
kubectl config view
```

# completion
```shell
kubectl completion bash
```

# nodes
```shell
kubectl get nodes
kubectl get nodes --show-labels
kubectl describe nodes minikube
kubectl label nodes minikube disktype=ssd
kubectl label nodes minikube disktype-
```
# port-foward
```shell
kubectl port-forward croc-hunter 8080:8080
```

# exec
```shell
kubectl exec -it croc-hunter /bin/sh
```

# create
```shell
kubectl create namespace croc-hunter
```

# get
```
kubectl get pods
kubectl get pods -n kube-system
kubectl get pods -o wide
kubectl describe pods kube-dns-v20-h15vs -n kube-system
kubectl get deploy,rs,pods
kubectl get pods croc-hunter -o yaml
kubectl get pods croc-hunter -o yaml
kubectl get svc,ep
```

# delete
```
kubectl delete pod redis-1828427801-rm9nd
```

# scale
```shell
kubectl scale deploy redis  --replicas=3
```

# explain
```
kubectl explain pods
```

# run
```
kubectl run redis --image=redis
kubectl run -i -t busybox --image=busybox --restart=Never
```

# base64
```shell
echo "YWRtaW4=" | base64 -D
echo "admin" | base64
```