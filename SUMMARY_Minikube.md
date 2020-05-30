# Minikube

### https://gist.github.com/invinciblycool/cef9547602fb25e2d6aeb7700d0dd4b1

## Installing Minikube KVM2

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo install minikube_latest_amd64 /usr/local/bin/minikube

sudo apt-get install -y qemu-kvm libvirt-bin bridge-utils
sudo apt-get install -y libvirt-clients libvirt-daemon-system
sudo usermod -a -G libvirt $(whoami) && newgrp libvirt

curl -LO https://storage.googleapis.com/minikube/releases/latest/docker-machine-driver-kvm2
sudo install docker-machine-driver-kvm2 /usr/local/bin/
```
## Starting minikube
```
minikube start --vm-driver=kvm2
```
## kubectl

https://kubernetes.io/docs/tasks/tools/install-kubectl/

## Alternative minikube install

```
sudo snap install minikube
```