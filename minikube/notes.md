# Minikube notes

```
minikube start
minikube tunnel
minikube stop
minikube ip

minikube addons enable dashboard
minikube addons enable ingress
minikube addons enable metrics-server
minikube addons list

minikube service --url -n drupal mysql
minikube service hello-node --url
# now you can access http://127.0.0.1:54252

# kubectl in a mode where it acts as a reverse proxy
kubectl proxy --port=8080
curl http://localhost:8080/api/

kubectl get namespaces --show-labels
kubectl config set-context --current --namespace=<namespace>
kubectl config view
kubectl get service
kubectl get services hello-node
kubectl get pods
kubectl get pods --output=wide
kubectl edit
kubectl describe
kubectl apply -f 
kubectl exec -it pod/NAME /bin/bash
kubectl port-forward service/mysql 3306:3306
```

## Links

- https://minikube.sigs.k8s.io/docs/
- https://minikube.sigs.k8s.io/docs/commands/
- https://kubernetes.io/docs/tasks/administer-cluster/
- https://kubernetes.io/docs/reference/kubectl/cheatsheet/
- https://minikube.sigs.k8s.io/docs/handbook/pushing/
