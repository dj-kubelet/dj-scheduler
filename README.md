# dj-scheduler
Makes sure only on pod at a time can run in each namespace.

## Deploy

```
docker build -t dj-scheduler .
kind load docker-image --name dj-kubelet dj-scheduler

kubectl create namespace dj-scheduler || true
kubectl apply -k "./dj-scheduler/development"
```
