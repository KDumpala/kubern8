## k8s Components
    1. Node
    2. Pod
    3. Service
    4. Ingress

## Nodes - 
   - Master Node
       - kube-apiserver: The front door and central management HUB.
       - etcd: Consistent key-value store for all cluster data and state.
       - kube-scheduler: Assigns Pods to healthy Worker Nodes based on resource constraints.
       - kube-controller-manager: Runs controllers that handle node failures, replication, endpoints, etc.
    
   - worker Node
       - kubelet: Agent that ensures containers are running in a Pod on the node.
       - kube-proxy: Maintains network rules on nodes to allow network communication.
       - Container Runtime: containerd


Cluster is the group(infra) of controlplane and worker nodes. -- > a.k.a Context during exam. 

`docker stop cka-cluster-control-plane cka-cluster-worker cka-cluster-worker2 kind-control-plane`

`docker start cka-cluster-control-plane cka-cluster-worker cka-cluster-worker2 kind-control-plane`

`kubectl` - command line tool for kubernetes cluster(any type).

`kubectl version --client`

`kubectl get nodes` -- list out nodes in cluster

`kubectl config get-contexts` -- list out clusters

`kubectl run nginx-pod --image=nginx:latest` -- impererative way, for creating pods with image

`kubectl create -f task.yaml` -- Declarative way of creating pods 

`kubectl delete pod nginx-pod` -- delete pod

`kubectl describe pod podname`  -- pod creation logs

`kubectl edit pod podname` -- edit the config runtime

`kubectl run nginx --image=nginx --dry-run=client -o yaml > task.yaml` -- dry run command and exports yaml output to task.yaml file 

`kubectl apply -f first_manifest.yaml` <-- apply the manifest/yaml file

`kubectl get all` -- returns all the objects running in the cluster
 

=====================
Replication controller - mostly for high availability or damage control

`kubectl get rc` -- to get the replication controller list

`kubectl scale --replicas=7 rs/nginx-rs` -- scale the pods imperative way

`kubectl edit rs/nginx-rs` -- replicaSet opens editor to make the changes in live, no apply command needed.

`kubectl create deploy deploy/nginx-new --image=nginx --dry-run=client -o yaml > .\imperative-commandtest.yaml`  -- for deployment.

`kubectl set image deployment/nginx nginx=nginx:1.23.4` -- update image during deployments

`kubectl rollout history deployment/nginx`  -- Check your rollout history to confirm the annotation was recorded


`kubectl annotate deployment/nginx kubernetes.io/change-cause="Pick up patch version" --overwrite`
`kubectl annotate deployment/nginx kubernetes.io/change-cause="Pick up patch version"` --  to assing a rollout change cause

`kubectl rollout undo deployment/nginx --to-revision=1`  -- to change th rollout change 