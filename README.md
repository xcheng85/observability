# observability
## Install minikube on Mac OS
https://medium.com/@seohee.sophie.kwon/how-to-run-a-minikube-on-apple-silicon-m1-8373c248d669
https://minikube.sigs.k8s.io/docs/start/

minikube start
minikube start --driver=docker --alsologtostderr

kubectl get po -A
minikube dashboard

kubectl create deployment hello-minikube --image=k8s.gcr.io/echoserver-arm:1.8
kubectl expose deployment hello-minikube --type=NodePort --port=8080

kubectl get services hello-minikube

kubectl port-forward service/hello-minikube 7080:8080


kubectl create deployment balanced --image=k8s.gcr.io/echoserver-arm:1.8 
kubectl expose deployment balanced --type=LoadBalancer --port=8080

minikube start --kubernetes-version=latest


