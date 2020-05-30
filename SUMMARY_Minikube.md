# Minikube

Installing KVM/QEMU

```
sudo apt-gte install -y qemu-kvm libvirt-bin bridge-utils virtinst virt-manager
```

Installing minikube (Debian package)
```
curl -LO https://storage.googleapis.com/minikube/releases/latest/minikube_latest_amd64.deb
sudo dpkg -i minikube_latest_amd64.deb
```