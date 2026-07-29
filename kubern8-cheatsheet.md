## k8s Components
    1. Node
    2. Pod
    3. Service
    4. Ingress

## Nodes - 
    Master Node
       - kube-apiserver: The front door and central management HUB.
       - etcd: Consistent key-value store for all cluster data and state.
       - kube-scheduler: Assigns Pods to healthy Worker Nodes based on resource constraints.
       - kube-controller-manager: Runs controllers that handle node failures, replication, endpoints, etc.
    worker Node
       - kubelet: Agent that ensures containers are running in a Pod on the node.
       - kube-proxy: Maintains network rules on nodes to allow network communication.
       - Container Runtime: containerd


Cluster is the group(infra) of controlplane and worker nodes. -- > a.k.a Context during exam. 

'kubectl get nodes' -- list out nodes in cluster
'kubectl config get-contexts' -- list out clusters

'kubectl run nginx-pod --image=nginx:latest' -- impererative way, for creating pods with image
'kubectl create -f task.yaml' -- Declarative way of creating pods 

'kubectl delete pod nginx-pod' -- delete pod

'kubectl describe pod podname'  -- pod creation logs

'kubectl edit pod podname' -- edit the config runtime

'kubectl run nginx --image=nginx --dry-run=client -o yaml > task.yaml' -- dry run command and exports yaml output to task.yaml file 

'kubectl apply -f first_manifest.yml' <-- apply the manifest

=====================
