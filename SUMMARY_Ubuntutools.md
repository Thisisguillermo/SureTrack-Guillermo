# Ubuntu tools

##  Tasksel

Tasksel is a Ubuntu—and Debian-specific tool, which helps to install multiple related packages as a coordinated task. Tasksel makes it incredibly easy to install related packages that make up the likes of:
- LAMP Server
- Mail Server
- Print Server
- Database servers
- Samba file server
- And more

### Commands

    sudo apt-get install tasksel -y

    sudo tasksel

source:

---

## [Infrastructure Code Deserves Tests Too See "Kitchen"](https://kitchen.ci)

Kitchen provides a test harness to execute infrastructure code on one or more platforms in isolation.

A driver plugin architecture is used to run code on various cloud providers and virtualization technologies such as Vagrant, Amazon EC2, and Docker. Read more

Many testing frameworks are supported out of the box including InSpec, Serverspec, and Bats

For Chef workflows, cookbook dependency resolution via Berkshelf or Policyfiles is supported or include a cookbooks/ directory and Kitchen will know what to do.

Kitchen is used by all Chef-managed community cookbooks and is the integration testing tool of choice for cookbooks.

---

## Creating virtual machines

Now that KVM is installed, let's see how we create our first VM. This can be done using:

- virt-manager: a GUI tool
- virt-install, a python script developed by Red Hat
- Vagrant

---

## [Build Automated Machine Images with Packer](https://www.packer.io/)

Packer is an open source tool for creating identical machine images for multiple platforms from a single source configuration. Packer is lightweight, runs on every major operating system, and is highly performant, creating machine images for multiple platforms in parallel. Packer does not replace configuration management like Chef or Puppet. In fact, when building images, Packer is able to use tools like Chef or Puppet to install software onto the image.

## [Development Environments Made Easy with Vagrant](https://www.vagrantup.com/)

HashiCorp Vagrant provides the same, easy workflow regardless of your role as a developer, operator, or designer. It leverages a declarative configuration file which describes all your software requirements, packages, operating system configuration, users, and more.