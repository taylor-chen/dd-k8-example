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

```bash
$ kubectl create -f agent.yaml
```

Verify DaemonSet

```bash
$ kubectl get daemonset
```