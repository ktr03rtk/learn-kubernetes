# start environment

minikube start --driver=virtualbox
minikube stop


# command
kubectl get pod,service,replicaset,deployment hoge
kubectl describe pod hoge
kubectl apply -f hoge.yml
kubectl run nginx-1 --image=nginx

kubectl create -f replicaset-definition.yml
kubectl replace -f replicaset-definition.yml
kubectl scale --replicas=6 -f replicaset-definition.yml
bubectl scale --replicas=6 replicaset(type) myapp-replicaset(name)
kubectl delete replicaset myapp-replicaset

