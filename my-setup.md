`winget install Kubernetes.kind` - install kind on win sys

`kind create cluster --image kindest/node:v1.36.1@sha256:3489c7674813ba5d8b1a9977baea8a6e553784dab7b84759d1014dbd78f7ebd5` - installs kind cluster

`kind --version` - check if kind is installed

`kubectl get nodes` - to check the nodes created

`kubectl config --set-context clustername` 

`kubectl config use-context my-cluster-name`

`kubectl config get-contexts`

`kubectl config current-contexts`           

`kubectl config use-context my-cluster-name`

`kubectl run nginx-pod --image=nginx:latest`

`kubectl get pods`

`kubectl describe pod nginx-pod`

`kubectl edit pod nginx-pod` - 

