```
docker build --platform linux/amd64 -t dogvatar-woof-works:v0 .
```

To test:

```
docker run -p 8080:8080 dogvatar-woof-works:v0
```

```
az acr login --name dogvatar
```

```
docker tag dogvatar-woof-works:v0 dogvatar.azurecr.io/dogvatar-woof-works:v0
```

```
docker push dogvatar.azurecr.io/dogvatar-woof-works:v0
```

ensure that the azure contrainer registry has permissions enabled for the app service. If already setup, there should be CI/CD for this push. TODO, automate build from a github action.
