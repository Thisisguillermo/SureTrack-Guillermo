# Insights

## Is CentOS still the Go to Distro for Servers?

https://www.reddit.com/r/linuxadmin/comments/gr2knx/is_centos_still_the_go_to_distro_for_servers/

CentOS repositories do not include metdata to categorize updates. This means it is impossible to setup email alerts for security updates only (possible via some hacks and community, but we’re talking corporate here). Also, Red Hat erratas are really useful for any security department, which CentOS lacks (again, there is a community one). Hardening guides for Linux are all for Red Hat, not CentOS (although most can be applied). Vendors always provide support for RHEL, not CentOS. In case of issues, a bad vendor could always put you off by saying “it’s your OS, not our application”

RHEL/CentOS are the go to distros for the enterprise world. While not ALL companies use it it's kind of like how VMware is the go to hypervisor solution for the enterprise world. It's just what people use . ( Side note Fedora is a branch off of CentOS/RHEL and is funded in part by redhat so that's also kind of included here for workstations ).

The concept behind RHEL is that it's stable like a Toyota would be, it just works and it will work until you run it into the ground. It's easy to manage through old school tools like ansible or puppet along with the even older scripted ssh . The reasons range from having slow non-essential updates and ensuring that packages are working and limited without adding more / extra repos.

From the enterprise support standpoint Redhat is a major player in the field and basically the original managed/ paid distribution company, they have a lot of trust and it gives companies someone to go after when their stuff isn't working...everyone likes someone else to blame .this relationship is similar to the VMware enterprise situation which I aluded to earlier, if you're familiar with it. Fun fact a lot of shared web hosting is RHEL / Centos also due to cpanel working best with it .

https://en.m.wikipedia.org/wiki/CPanel (The latest cPanel & WHM version supports installation on CentOS, Red Hat Enterprise Linux (RHEL), and CloudLinux OS.[5] cPanel 11.30 is the last major version to support FreeBSD.[6][7])

I would also argue that Ubuntu is extremely popular as the next largest , it often shows as first I think due to the bots scanning and not differentiating completely between enterprise servers , workstations , home computers and containers. I will say that centos doesn't work so well for docker containers in my experience but is pretty good for lxc. There are just lighter options for running CTs..not that they are really used in many on prem prod deployments anyway .

Either Ubuntu server or CentOS will be fine , but if you want to make your life easy pick one and stick to it because they use different package management and install methods + have different application versions usually . Further if you're a company and want good support / to blame someone when you don't want to waste your time troubleshooting annoying issues for hours and or work with VMware redhat is probably your best bet.

Redhat has some data here https://www.redhat.com/en/blog/red-hat-continues-lead-linux-server-market

Techradar has it as #2 here https://www.techradar.com/best/best-linux-server-distro

You can see it as #2 here also https://w3techs.com/technologies/details/os-linux

See also https://w3techs.com/technologies/details/os-centos

All my 2c . Now that you've read all of that -- I use ubuntu server on my homelab and centos ... I find them both great but having worked in an all RHEL/ centos shop I can say I prefer Ubuntu as a workstation install . I just find ubuntu and other Debian based distros more up to date for daily non-server use.

Also mobile. Excuse typos and such.

---

## Is Debian the gold standard for Linux security?

https://www.infoworld.com/article/3118898/is-debian-the-gold-standard-for-linux-security.html


## Container Management

### Minikube

Minikube can run on Windows and MacOS, because it relies on virtualization (e.g. Virtualbox) to deploy a kubernetes cluster in a Linux VM. You can also run minikube directly on linux with or without virtualization. It also has some developer-friendly features, like add-ons.

Minikube is currently limited to a single-node Kubernetes cluster (for details, see this issue). Although, it is on their roadmap.

### Microk8s

Disclaimer: of all the K8s offerings, I know the least about this one

Microk8s is similar to minikube in that it spins up a single-node Kubernetes cluster with its own set of add-ons.

Like minikube, microk8s is limited to a single-node Kubernetes cluster, with the added limitation of only running on Linux and only on Linux where snap is installed.

### K3s

K3s runs on any Linux distribution without any additional external dependencies or tools. It is marketed by Rancher as a lightweight Kubernetes offering suitable for edge environments, IoT devices, CI pipelines, and even ARM devices, like Raspberry Pi's. K3s achieves its lightweight goal by stripping a bunch of features out of the Kubernetes binaries (e.g. legacy, alpha, and cloud-provider-specific features), replacing docker with containerd, and using sqlite3 as the default DB (instead of etcd). As a result, this lightweight Kubernetes only consumes 512 MB of RAM and 200 MB of disk space. K3s has some nice features, like Helm Chart support out-of-the-box.

Unlike the previous two offerings, K3s can do multiple node Kubernetes cluster. However, due to technical limitations of SQLite, K3s currently does not support High Availability (HA), as in running multiple master nodes. The K3s team plans to address this in the future.

Now, on to some honorary mentions...

### Kind

Kind (Kubernetes-in-Docker), as the name implies, runs Kubernetes clusters in Docker containers. This is the official tool used by Kubernetes maintainers for Kubernetes v1.11+ conformance testing. It supports multi-node clusters as well as HA clusters. Because it runs K8s in Docker, kind can run on Windows, Mac, and Linux.

Kind is optimized first and foremost for CI pipelines, so it may not have some of the developer-friendly features of other offerings.

### Desktop Docker

Docker for Mac/Windows now ships with a bundled Kubernetes offering.

However:

    Kubernetes versions are tightly coupled with the Docker version (i.e. Docker stable channel ships with K8s v1.10. If you want K8s v1.13, you need to switch to Docker edge channel).

    Not as easy to destroy and start a new K8s cluster. AFAIK, you would have to disable Kubernetes and re-enable it through the Docker desktop app preferences.

### K3d

A new project that aims to bring K3s-in-Docker (similar to kind).

They're still working through some issues, like exposing the right docker ports ...etc.

### Kubeadm

The official CNCF tool for provisioning Kubernetes clusters in a variety of shapes and forms (e.g. single-node, multi-node, HA, self-hosted)

Although this is the most manual way to create and manage a cluster of all the offerings listed here.

... And there are plenty more that I do not remember off the top of my head.