# dd-k8-example

The goal with this project is to demonstrate Datadog features on Kubernetes with boilerplate instrumentation.

## Local Dev

### What you need

- Minikube
- Docker
- Datadog account, a trial account is sufficient

    - Get your API key. https://app.datadoghq.com/account/settings#api



### Getting Started with Minikube

For local dev, we are using Minikube.


```bash
$ minikube start
```

RBAC permissions

```bash
$ kubectl create -f rbac
```

Agent manifest

Update the `DD_API_KEY` env value before running:

```bash
$ kubectl create -f agent.yaml
```

Verify DaemonSet

```bash
$ kubectl get daemonset
```

