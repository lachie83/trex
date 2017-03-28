# Create pdb
```shell
kubectl create -f pdb-example.yaml
```

# View pdb
```shell
kubectl get poddisruptionbudget
```

# Start kubectl proxy to kube-api
```shell
kubectl proxy -p 8080 &
```

# Attempt eviction
```shell
curl -v -H 'Content-type: application/json' http://127.0.0.1:8080/api/v1/namespaces/default/pods/croc-hunter-838257170-9c7x2/eviction -d @pdb-eviction.json
```