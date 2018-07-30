# Notes on how to install and setup K8s cluster on local machine (tested on Mac OS)

## Prerequisites
 - kubectl
 - docker (for Mac) - optional
 - minikube
 - hyperkit


OS: MacOS
VM Driver: hyperkit
ISO version: v0.23.6
Minikube: v0.28.1

## Hyperkit

Install Hyperkit

```
brew install hyperkit
```

## Kubernetes

Install Kubernetes (https://kubernetes.io/docs/tasks/tools/install-kubectl/):

```
brew install kubernetes-cli
```

## Minikube

Given the known issue of VirtualBox conflicts with Hyperkit, make sure no VirtualBox processes are running
```
ps -ef | grep -Ei "vbo[x]|virtualbo[x]"
```

Install Minikube (https://github.com/kubernetes/minikube/releases):

```
curl -Lo minikube https://storage.googleapis.com/minikube/releases/v0.28.1/minikube-darwin-amd64 && chmod +x minikube && sudo mv minikube /usr/local/bin/
```

Start minikube

```
minikube start --loglevel=0 --logtostderr --v=10 --vm-driver hyperkit
```

Status:
```
minikube ssh sudo systemctl is-active kubelet
```



### Troubleshooting




## References:

https://github.com/kubernetes/minikube/issues/1618
https://github.com/kubernetes/minikube/issues/2765
https://github.com/kubernetes/minikube/issues/2127
https://github.com/kubernetes/minikube/issues/2456
https://github.com/kubernetes/minikube/issues/2841
https://github.com/kubernetes/minikube/issues/2554
https://github.com/kubernetes/kubernetes/issues/53333
https://github.com/kubernetes/kubernetes/issues/44665

---
