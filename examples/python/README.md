# Python

```bash
eval $(minikube docker-env)
```


from this directory, run:

```bash
docker build -t hello-flask:latest .
```

hello-flask should now exists in Minikube's Docker registry:
```bash
    minikube ssh docker images 
```

deploy and create a service:

```bash
kubectl create -f flask.yaml 
kubectl create -f flask-service.yml
```

The new deployment will be autodiscovered in Datadog.