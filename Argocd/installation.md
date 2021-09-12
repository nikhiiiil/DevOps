### Official Docs to install Argocd

* getting started https://argoproj.github.io/argo-cd/getting_started/


## Steps to install Argocd

```

>> kubectl create namespace argocd

>> kubectl apply -n argocd -f https://raw.githubusercontent.com/argoproj/argo-cd/stable/manifests/install.yaml

>> kubectl patch svc argocd-server -n argocd -p '{"spec": {"type": "LoadBalancer"}}'
   
>> kubectl port-forward svc/argocd-server -n argocd 8080:443
   (Export service if service type is clusterIP)

```