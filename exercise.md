
Exercise 1 - creating pods - https://github.com/piyushsachdeva/CKA-2024/blob/main/Resources/Day07/task.md

kubectl run nginx-pod --image=nginx:latest
kubectl run nginx --image=nginx --dry-run=client -o yaml > task.yaml
kubectl describe pod redis
kubectl apply -f task.yaml

############################

Exercise 2 - https://github.com/piyushsachdeva/CKA-2024/blob/main/Resources/Day08/task.md

kubectl create deploy nginx --image=nginx:1.23.0 --dry-run=client -o yaml > .\imperative-commandtest.yaml 
kubectl get pods
- open yaml and update version to 1.23.4
kubectl describe pod podname
kubectl annotate deployment/nginx kubernetes.io/change-cause="Pick up patch version"
kubectl scale --replicas=5 deployment/nginx     
kubectl rollout undo deployment/nginx --to-revision=1   