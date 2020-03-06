# Kubernetes example project

It's for Udemy https://www.udemy.com/course/docker-and-kubernetes-the-complete-guide

## Installation

ingress-nginx

https://github.com/kubernetes/ingress-nginx

Run once:
``` 
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.30.0/deploy/static/mandatory.yaml
```

For Docker for Mac run also:

``` 
kubectl apply -f https://raw.githubusercontent.com/kubernetes/ingress-nginx/nginx-0.30.0/deploy/static/provider/cloud-generic.yaml
```

Verify installation:
``` 
kubectl get pods --all-namespaces -l app.kubernetes.io/name=ingress-nginx --watch
```

## Start project

Start k8s cluster
```
kubectl apply -f k8s
```

Start skaffold
```
skaffold dev
```

## Check

Check services
```
kubectl get ingress,services,pods,pvc,pv
```

Check secrets
``` 
kubectl get secrets
```
