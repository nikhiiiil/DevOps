# Setting up kubernates cluster

## Setting minikube [single node cluster]

### Requirements:

* install kubectl.exe https://kubernetes.io/docs/tasks/tools/install-kubectl-windows/#install-kubectl-binary-with-curl-on-windows

* install MiniKube https://v1-18.docs.kubernetes.io/docs/tasks/tools/install-minikube/

* Oracle Vm  or any Hypervisor https://www.oracle.com/virtualization/technologies/vm/downloads/virtualbox-downloads.html

* minikube official doc https://minikube.sigs.k8s.io/docs/start/

### Note:
* Keep kubectl.exe and minikube.exe on same location

## How to start minikube:

```
>> minikube.exe start
   This will download minikube image which internally has all things for a single node cluster.

>> kubectl expose deployment hello-node --type=LoadBalancer --port=8080

>> kubectl get deployment,svc,pods

>> kubectl delete service hello-node

>> kubectl delete deployment hello-node

>> minikube stop

>> minikube delete

```

## Cheat Sheet for Kubectl

* https://kubernetes.io/docs/reference/kubectl/cheatsheet/

## AddOn's for minikube

* minikube addons enable ingress