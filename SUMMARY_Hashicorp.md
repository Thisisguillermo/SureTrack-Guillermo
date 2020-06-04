# Hashicorp Software

## Vagrant

Vagrant is for development environments.

Vagrant provides a number of higher level features that Terraform doesn't. Synced folders, automatic networking, HTTP tunneling, and more are features provided by Vagrant to ease development environment usage. Because Terraform is focused on infrastructure management and not development environments, these features are out of scope for that project.

## Back-upp vagrant boxes

https://stackoverflow.com/questions/43411734/correct-way-to-back-up-and-restore-vagrant-box-variable-vvv

You can package your working VM into a new vagrant box

`vagrant package --output ./new-box-name.box`

`vagrant package`

and then backup this box

After you reinstall your Mackbook, you can then add this box to your local vagrant directory

`vagrant box add new-box-name ./new-box-name.box`

`vagrant box add package.box --name yourname_box`

After that you initiate the vagrantfile through

`vagrant init newbox`

`vagrant init yourname_box`

`vagrant up`

### Vagrant boxes (Libvirt)

vagrant init generic/ubuntu1804

vagrant init peru/ubuntu-18.04-desktop-amd64 \ --box-version 20200401.01

vagrant init abi/ubuntu2004

vagrant init generic/rhel8

vagrant init generic/centos8

vagrant init centos/7

### Vagrant git

https://www.youtube.com/watch?v=epk-fkdLaIg

```ruby
Vagrant.configure("2") do |config|
  config.ssh.private_key_path = "~/.ssh/id_rsa"
  config.ssh.forward_agent = true
end
```

# Vagrant hostmanager plugins

https://github.com/devopsgroup-io/vagrant-hostmanager

# Vagrant mutate

https://github.com/sciurus/vagrant-mutate


```
Virtualbox to kvm
Virtualbox to libvirt
Virtualbox to bhyve
Libvirt to kvm
Kvm to libvirt
```

## Terraform

Terraform is for setting and managing the (cloud) infrastructure.
Infrastructure as code.

"Use Infrastructure as Code to provision and manage any cloud, infrastructure, or service"


dsfgadssfasd