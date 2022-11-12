Для установки приложения нужно проделать следующие шаги: <br/>
1. ```kubectl create namespace m && helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx/ && helm repo update && helm install nginx ingress-nginx/ingress-nginx --namespace m -f ingress/nginx-ingress.yaml```
2. ```kubectl apply -f manifests/ ```

Для проверки, что приложение работает нужно выполнить следующую команду: <br/>
```curl http://arch.homework/health```

Для удаления приложения нужно выполнить команду: <br/>

```kubectl delete namespace m```