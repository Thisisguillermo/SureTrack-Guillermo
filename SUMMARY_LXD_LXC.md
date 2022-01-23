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

/var/snap/lxd/common/lxd/disks and /var/snap/lxd/common/lxd/images

`lxc list`

### Create a backup of www-vm on server1 (https://www.cyberciti.biz/faq/how-to-movemigrate-lxd-vm-to-another-host-on-linux/)

`sudo tar -zcvf /root/www-vm.tar.gz /var/lib/lxd/storage-pools/default/containers/www-vm/`

##### Copy www-vm-tar.gz from server1 to server2

`sudo scp /root/www-vm.tar.gz root@server2:/root/` or `sudo rsync -v /root/www-vm.tar.gz root@server2:/root/`

##### Restore backup file named www-vm-tar.gz on server2

```sudo -i
cd /var/lib/lxd/storage-pools/default/containers/
tar -zxvf /root/www-vm-tar.gz
```

##### Finally, create a soft-link using ln command, run:

```
cd /var/lib/lxd/containers/
ln -s /var/lib/lxd/storage-pools/default/containers/www-vm/
```

##### Restore and import container on server2

*LXD maintains a backup.yaml file in each container’s storage volume. Use this to recover or restore a given container, such as container configuration, attached devices and storage. This file can be processed by the following command:*

```
lxd import {containerNameHere}
lxd import www-vm
```

