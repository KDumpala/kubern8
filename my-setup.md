`winget install Kubernetes.kind` - install kind package on win sys

`kind create cluster --image kindest/node:v1.36.1@sha256:3489c7674813ba5d8b1a9977baea8a6e553784dab7b84759d1014dbd78f7ebd5` - installs kind cluster

`kind --version` - check if kind is installed

`kubectl get nodes` - to check the nodes created

`kubectl config --set-context clustername` Creates or modifies a context entry in your configuration file.

`kubectl config use-context my-cluster-name` Switches your active context (cluster/user/namespace combination).

`kubectl config get-contexts` Lists all defined contexts available in your configuration.

`kubectl config current-contexts` (typically current-context) Displays the name of the currently active context.

`kubectl run nginx-pod --image=nginx:latest` Creates and runs a single Pod named nginx-pod using the nginx:latest image.

`kubectl get pods` Lists all Pods in the current namespace along with their status.

`kubectl describe pod nginx-pod` Shows detailed configuration, state, and recent lifecycle events for nginx-pod.

`kubectl edit pod nginx-pod` Opens the live YAML manifest of nginx-pod in a text editor to make direct updates.

`kubectl exec -it nginx-pod -- sh` - logs you into the pod as shell

`kubectl get pods nginx-pod --show-labels` : shows labels atatched to the pod

`kubectl get pods -o wide` - gives you extra details about the pod running 

`docker stop cka-cluster-control-plane cka-cluster-worker cka-cluster-worker2 kind-control-plane`

`docker start cka-cluster-control-plane cka-cluster-worker cka-cluster-worker2 kind-control-plane`