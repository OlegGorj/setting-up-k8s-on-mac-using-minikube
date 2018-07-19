# Notes on how to install and setup K8s cluster on local machine (macOs)

## Prerequisites
 - kubectl
 - docker (for Mac)
 - minikube
 - virtualbox


OS: MacOS
VM Driver: virtualbox
ISO version: v0.23.6
Minikube: v0.28.1

## VirtualBox

## Kubernetes

## Minikube

Start minikube

```
--vm-driver=virtualbox --loglevel 0 --alsologtostderr --extra-config=apiserver.service-node-port-range=90-32000 --v=0
```

Status:
```
minikube ssh sudo systemctl is-active kubelet
```



### Troubleshooting

Login to VBox:

```
minikube ssh bash
```

In the machine:

```
bash-4.4$ sudo su -

# docker ps
CONTAINER ID        IMAGE                                     COMMAND                  CREATED             STATUS              PORTS               NAMES


```



## References:

https://github.com/kubernetes/minikube/issues/1618
https://github.com/kubernetes/minikube/issues/2765

---
