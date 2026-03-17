# Домашнее задание к занятию `«Сетевое взаимодействие в K8S. Часть 2»` - `Демин Герман`

## Задание 1

`nano frontend-deployment.yaml`

[frontend-deployment.yaml](frontend-deployment.yaml)

`nano backend-deployment.yaml`

[backend-deployment.yaml](backend-deployment.yaml)

`kubectl get pods`

`kubectl exec -it frontend-78dc97d455-4242j -- bash`

`curl backend-service:8080`

![curl-1](/img/curl-1.png)

`kubectl exec -it backend-787749949f-g4c96 -- bash`

`curl frontend-service:80`

![curl-2](/img/curl-2.png)



## Задание 2

`minikube addons enable ingress`

`kubectl get pods -n kube-system`

`nano ingress-service.yaml`

[ingress-service.yaml](ingress-service.yaml)

`kubectl apply -f ingress.yaml`

`kubectl get ingress`

`minikube ip`

![ip](/img/ip.png)

`curl http://192.168.49.2/`

`curl http://192.168.49.2/api`

![kube-1](/img/kube-1.png)
