# Create deployment to apply hpa
```shell
kubectl create -f hpa-deployment-example.yaml
```

# Create HPA
```shell
kubectl autoscale deployment croc-hunter --min=3 --max=5 --cpu-percent=20
```

# Check HPA status
```shell
kubectl get hpa
```