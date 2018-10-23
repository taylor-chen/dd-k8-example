# dd-k8-example

Example project with k8

## Local Dev

### Using Minikube

For local dev, use Minikube.

https://kubernetes.io/docs/tasks/tools/install-minikube/

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

