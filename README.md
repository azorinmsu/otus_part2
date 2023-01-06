Для установки приложения нужно проделать следующие шаги: <br/>
1. ```kubectl create namespace m && helm repo add ingress-nginx https://kubernetes.github.io/ingress-nginx/ && helm repo update && helm install nginx ingress-nginx/ingress-nginx --namespace m -f ingress/nginx-ingress.yaml```
2. ```
   helm repo add bitnami https://charts.bitnami.com/bitnami && helm install my-release  \
    --set auth.username=otus,auth.password=otus,auth.database=mongo \
    my-repo/mongodb
   ```
3. ```
   kubectl create secret generic spring-security \
   --from-literal=spring.mongo.dbname=mongo \
   --from-literal=spring.mongo.password=otus \
   --from-literal=spring.mongo.username=otus \ 
   --from-literal=spring.mongo.port=27017
   ```
4. ```kubectl apply -f manifests/ ```

Для проверки, что приложение работает нужно выполнить следующую команду: <br/>
```curl http://arch.homework/health```

Для удаления приложения нужно выполнить команду: <br/>

```kubectl delete namespace m```