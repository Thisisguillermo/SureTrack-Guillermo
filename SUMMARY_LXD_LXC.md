# LXD/LXC (https://linuxcontainers.org/lxd/getting-started-cli/)

```
sudo dnf install snapd

sudo ln -s /var/lib/snapd/snap /snap

sudo systemctl restart snapd.service

sudo snap install lxd

sudo snap enable lxd

sudo snap start lxd

sudo usermod -a -G lxd $USER
```

### Download images and launch images

`lxc image list images:`

`lxc image list images: 'alpine'`

```
lxc launch images:alpine/3.8/amd64 alpine-www
lxc launch images:centos/7/amd64 cenots-db
lxc launch images:opensuse/15.0/amd64 opensuse-15
lxc list
```

### Use container

`sudo lxc exec ample-pangolin -- bash`

### Physical image location

/var/snap/lxd/common/lxd/disks and /var/snap/lxd/common/lxd/images

### Migrate

https://www.cyberciti.biz/faq/how-to-movemigrate-lxd-vm-to-another-host-on-linux/