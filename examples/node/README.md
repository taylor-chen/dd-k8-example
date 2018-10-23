# Node.JS

from https://kubernetes.io/docs/tutorials/hello-minikube/

```bash
eval $(minikube docker-env)
```


from this directory, run:

```bash
docker build -t hello-node:v1 .
```

hello-node should now exists in Minikube's Docker registry:
```bash
minikube ssh docker images 
```

deploy:

```bash
kubectl run hello-node --image=hello-node:v1 --port=8080 --image-pull-policy=Never
```

The new deployment will be autodiscovered in Datadog.