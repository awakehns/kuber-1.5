# Домашнее задание к занятию `«Сетевое взаимодействие в K8S. Часть 2»` - `Демин Герман`

## Задание 1

`nano frontend-deployment.yaml`

[frontend-deployment.yaml](frontend-deployment.yaml)

`nano backend-deployment.yaml`

[backend-deployment.yaml](backend-deployment.yaml)

![kube-2](/img/kube-2.png)

`kubectl get pods`

`kubectl exec -it frontend-78dc97d455-4242j -- bash`

`curl backend-service:8080`

`kubectl exec -it backend-787749949f-g4c96 -- bash`

`curl frontend-service:80`



## Задание 2

`minikube addons enable ingress`

`kubectl get pods -n kube-system`

`nano ingress-service.yaml`

[ingress-service.yaml](ingress-service.yaml)

`kubectl apply -f ingress.yaml`

`minikube tunnel`

`kubectl get ingress`

![kube-1](/img/kube-1.png)
