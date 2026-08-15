# kubernetes-minikube

A repo for working with the Kubernetes Minikube clusters.

## Steps

Mac (Homebrew): brew install minikube kubectl
Windows (Chocolatey): choco install minikube kubernetes-cli
Linux: Follow the quick binary downloads on the official Kubernetes site.

- minikube start
- kubectl apply -f deployment.yaml
- kubectl apply -f service.yaml
- kubectl get pods -w
- kubectl port-forward service/hello-poc-service 9000:8080
- kubectl delete service hello-poc-service
- kubectl delete deployment hello-poc-service
- minikube stop

### Troubleshooting pods

kubectl logs hello-poc-service-instance-name
kubectl describe pod hello-poc-service-instance-name

### Notes

- a Pod is a pre-configured group of running Docker containers that share the exact same network and storage
