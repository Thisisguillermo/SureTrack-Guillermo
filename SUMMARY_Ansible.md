# Ansible

## Example: How to Use Ansible to Automate Initial Server Setup on Ubuntu 18.04

https://www.digitalocean.com/community/tutorials/how-to-use-ansible-to-automate-initial-server-setup-on-ubuntu-18-04

## Ansible provsioner vagrant

https://www.vagrantup.com/docs/provisioning/ansible.html

## Run ad hoc Ansible commands in Vagrant

`ansible all -i vagrant_ansible_inventory_default -u vagrant --private-key ~/.vagrant.d/insecure_private_key -m ping`



I was missing Vagrant's private ssh key. Found that here: stackoverflow.com/a/18943360/503463

There are a couple ways to do this, but here's what I'm using:

ansible all -i vagrant_ansible_inventory_default -u vagrant --private-key ~/.vagrant.d/insecure_private_key -m ping

Everything before -m is essentially boilerplate. I'm using a standard box with the default username 'vagrant'. The flag -i vagrant_ansible_inventory_default tells Ansible to use the inventory file generated by Vagrant; it contains one host, so targeting all is safe ('default' also works). Finally, we pass the Vagrant private key to authenticate the ssh connection: --private-key ~/.vagrant.d/insecure_private_key

Also, you can add the user and private key directly to the inventory file, using the ansible_ssh_user and ansible_ssh_private_key_file parameters, so you don't have to enter those all the time. See List of Behavioral Inventory Parameters http://docs.ansible.com/intro_inventory.html#list-of-behavioral-inventory-parameters