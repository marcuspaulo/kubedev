
# Exercícios

## ​Crie 3 ambientes para a sua API: Developer, Stage e Production. Cada ambiente deve ter as suas respectivas configurações de ambiente.​


# Criando ambiente MongoDB Developer
## Criando o Namespace
```sh
kubectl create namespace developer
```

## Criando o MongoDB Secret
```sh
kubectl apply -f mongodb/mongodb-secret.yaml
```

## Criando o Deployment MongoDB
```sh
kubectl apply -f mongodb/deployment.yaml 
```

## Criando o Service MongoDB
```sh
kubectl apply -f mongodb/service.yaml 
```
<hr>
# Criando ambiente API Developer

## Criando o API Secret
```sh
kubectl apply -f api/api-configmap.yaml 
```

## Criando o Deployment API
```sh
kubectl apply -f api/deployment.yaml 
```

## Criando o Service API
```sh
kubectl apply -f api/service.yaml 
```

## Para testar 
```sh
kubectl port-forward service/api-service 31822:80
```

URL: http://127.0.0.1:31822/swagger/index.html

<hr><hr>

# Criando ambiente MongoDB Stage
## Criando o Namespace
```sh
kubectl create namespace stage
```

## Criando o MongoDB Secret
```sh
kubectl apply -f mongodb/mongodb-secret.yaml
```

## Criando o Deployment MongoDB
```sh
kubectl apply -f mongodb/deployment.yaml 
```

## Criando o Service MongoDB
```sh
kubectl apply -f mongodb/service.yaml 
```
<hr>
# Criando ambiente API Stage

## Criando o API Secret
```sh
kubectl apply -f api/api-configmap.yaml 
```

## Criando o Deployment API
```sh
kubectl apply -f api/deployment.yaml 
```

## Criando o Service API
```sh
kubectl apply -f api/service.yaml 
```

## Para testar 
```sh
kubectl port-forward service/api-service 31822:80
```

URL: http://127.0.0.1:31822/swagger/index.html

<hr><hr>

# Criando ambiente MongoDB Production
## Criando o Namespace
```sh
kubectl create namespace production
```

## Criando o MongoDB Secret
```sh
kubectl apply -f mongodb/mongodb-secret.yaml
```

## Criando o Deployment MongoDB
```sh
kubectl apply -f mongodb/deployment.yaml 
```

## Criando o Service MongoDB
```sh
kubectl apply -f mongodb/service.yaml 
```
<hr>
# Criando ambiente API Production

## Criando o API Secret
```sh
kubectl apply -f api/api-configmap.yaml 
```

## Criando o Deployment API
```sh
kubectl apply -f api/deployment.yaml 
```

## Criando o Service API
```sh
kubectl apply -f api/service.yaml 
```

## Para testar 
```sh
kubectl port-forward service/api-service 31822:80
```

URL: http://127.0.0.1:31822/swagger/index.html



