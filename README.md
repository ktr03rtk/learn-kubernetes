# start environment

- minikube start --driver=virtualbox
- minikube stop
- minikube service list


# command
- kubectl get pod,service,replicaset,deployment hoge
- kubectl describe pod hoge
- kubectl apply -f hoge.yml
- kubectl run nginx-1 --image=nginx

### replicaset

- kubectl create -f replicaset-definition.yml --record
- kubectl replace -f replicaset-definition.yml
- kubectl scale --replicas=6 -f replicaset-definition.yml
- bubectl scale --replicas=6 replicaset(type) myapp-replicaset(name)
- kubectl delete replicaset myapp-replicaset


### deployment

- kubectl rollout status deployment  myapp-deployment
- kubectl edit deployment myapp-deployment
- kubectl rollout history deployment  myapp-deployment
- kubectl rollout undo deployment

### service

- kubectl create -f pod.yml
- kubectl create -f node_port_service.yml
- kubectl get service → get the port
- minikube service list → get the node ip
- minikube service myapp-service --url
