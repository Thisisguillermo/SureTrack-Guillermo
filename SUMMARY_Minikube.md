# Minikube

Installing KVM/QEMU

```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo install minikube_latest_amd64 /usr/local/bin/minikube

sudo apt-get install -y qemu-kvm libvirt-bin bridge-utils virtinst virt-manager
sudo usermod -a -G libvirt $(whoami)
newgrp libvirt

curl -LO https://storage.googleapis.com/minikube/releases/latest/docker-machine-driver-kvm2
sudo install docker-machine-driver-kvm2 /usr/local/bin/

```