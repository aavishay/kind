# Deploy a KinD cluster locally
```
kind create cluster --name test --config kind-config.yaml
```

# Deploy a Docker registry locally
```
docker run -d -p 127.0.0.1:5001:5000 --restart=always --name kind-registry registry:2
```
# Connect KinD to Docker registry
```
docker network connect kind kind-registry
```