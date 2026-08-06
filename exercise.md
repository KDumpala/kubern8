
Exercise 1 - creating pods 

kubectl run nginx-pod --image=nginx:latest
kubectl run nginx --image=nginx --dry-run=client -o yaml > task.yaml
kubectl describe pod redis
kubectl apply -f task.yaml

############################

Exercise 2 -

