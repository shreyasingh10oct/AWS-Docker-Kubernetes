# Commands for Docker and Kubernetes

## Build Docker Image

```bash
docker build -t shreya_sklearn .
# docker build -t instructor_sklearn .
```

## Run Docker Image (Locally to test)

```bash
docker run --name shreya_sklearn shreya_sklearn
# docker run -it --name sklearn_01 -dt instructor_sklearn /bin/bash
# docker run -it instructor_sklearn /bin/bash

docker exec -it shreya_sklearn shreya_sklearn
# docker exec -it sklearn_01 /bin/bash
```

## Push to Azure Container Registry

```bash
az acr login --name crdsba6190deveastus001
# az acr login --name crdsba6190deveastus001
docker tag shreya_sklearn crdsba6190deveastus001.azurecr.io/shreya_sklearn
# docker tag instructor_sklearn crdsba6190deveastus001.azurecr.io/instructor_sklearn
docker push crdsba6190deveastus001.azurecr.io/shreya_sklearn
# docker push crdsba6190deveastus001.azurecr.io/instructor_sklearn
```

## Apply Kubernetes Pod

```bash
kubectl apply -f <POD YAML FILE>
# kubectl apply -f example_pod.yml
```

## Remote into Pod 

```bash
kubectl exec -it <pod_name> -- /bin/bash
# kubectl exec -it instructor-test-01 -- /bin/bash
```