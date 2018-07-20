# Notes on how to install and setup K8s cluster on local machine (macOs)

## Prerequisites
 - kubectl
 - docker (for Mac)
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

## Minikube

Make sure no VirtualBox processes are running
```
ps -ef | grep -Ei "vbo[x]|virtualbo[x]"
```

Start minikube

```
start --loglevel=0 --logtostderr --v=10 --vm-driver hyperkit
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

---
