# Minikube Debian

### https://gist.github.com/invinciblycool/cef9547602fb25e2d6aeb7700d0dd4b1

## Installing minikube KVM

```

sudo apt install -y curl
sudo apt install -y virt-manager
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo install minikube_latest_amd64 /usr/local/bin/minikube

`sudo apt install ./minikube_latest_amd64.deb`
```


##  installing minikube virtualbox
```
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

# Install kubectl

```
sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
```

## Alternative minikube install

```
sudo snap install minikube
```