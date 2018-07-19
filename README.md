# Notes on how to install and setup K8s cluster on local machine (macOs)

OS: MacOS
VM Driver: virtualbox
ISO version: v0.23.6
Minikube: v0.28.1

## VirtualBox

## Kubernetes

## Minikube

## Start minikube

```
minikube start --bootstrapper=localkube --vm-driver=virtualbox --docker-opt="default-ulimit=nofile=102400:102400"
```

### Troubleshooting

Login to VBox:
```
minikube ssh bash
```




## References:


---
