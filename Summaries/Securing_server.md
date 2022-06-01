# Securing Linux servers.

## https://www.cyberciti.biz/tips/linux-security.html

## https://www.cisecurity.org/

The Center for Internet Security, a non-profit whose mission is to promote internet security best-practices, created a step-by-step checklist for securing Docker. Subsequently, the Docker team released a security auditing tool – Docker Bench for Security – to run through this checklist on a Docker host and flag any issues it finds

## Lynis

https://github.com/CISOfy/lynis

Lynis - Security auditing and hardening tool, for UNIX-based systems.

Lynis is a security auditing tool for systems based on UNIX like Linux, macOS, BSD, and others. It performs an in-depth security scan and runs on the system itself. The primary goal is to test security defenses and provide tips for further system hardening. It will also scan for general system information, vulnerable software packages, and possible configuration issues. Lynis was commonly used by system administrators and auditors to assess the security defenses of their systems. Besides the "blue team," nowadays penetration testers also have Lynis in their toolkit.

## cve-check-tool

cve-check-tool, as its name suggests, is a tool for checking known (public) CVEs. The tool will identify potentially vunlnerable software packages within Linux distributions through version matching. Where possible it will also seek to determine (through a distribution implemention) if a vulnerability has been addressed by way of a patch.

## https://github.com/imthenachoman/How-To-Secure-A-Linux-Server

Turn on SELinux (enabled by default)
Security-Enhanced Linux (SELinux) is an access control security mechanism provided in the kernel.

Disable password authentication to the server

No root login

Passwordless login with SSH key ED25519.

It's not using a password for SSH with 2FA through app.

Proxy server

Firewall

Unattended updates security updates (https://www.howtoforge.com/tutorial/how-to-setup-automatic-security-updates-on-centos-7/)

Fail 2 ban

Port knocking (https://wiki.archlinux.org/index.php/Port_knocking)

Secure Shared Memory (https://blog.runcloud.io/how-to-secure-your-linux-server/)

Mode evasive (https://hostadvice.com/how-to/how-to-secure-apache-web-server-with-modevasive-on-ubuntu-18-04-vps/)

Denyhosts (https://linuxhint.com/install-denyhosts-on-ubuntu/)

Port Scanning Attack Detection (https://www.digitalocean.com/community/tutorials/how-to-use-psad-to-detect-network-intrusion-attempts-on-an-ubuntu-vps)

Jumphost (https://www.madboa.com/blog/2017/11/02/ssh-proxyjump/) (https://www.tecmint.com/access-linux-server-using-a-jump-host/amp/) (https://www.techrepublic.com/article/how-to-use-ssh-to-proxy-through-a-linux-jump-host/) (https://en.wikibooks.org/wiki/OpenSSH/Cookbook/Proxies_and_Jump_Hosts)

Greynoise filter https://greynoise.io/about
Mass scanners (such as Shodan and Censys), search engines, bots, worms, and crawlers generate logs and events omnidirectionally on every IP address in the IPv4 space. GreyNoise gives you the ability to filter this useless noise out.

Docker Bench for Security

https://github.com/docker/docker-bench-security

The Docker Bench for Security is a script that checks for dozens of common best-practices around deploying Docker containers in production. The tests are all automated, and are inspired by the CIS Docker Community Edition Benchmark v1.1.0.



For extra security https://www.cyberciti.biz/tips/linux-security.html


## Web security.

https://speakerdeck.com/filedescriptor/exploiting-the-unexploitable-with-lesser-known-browser-tricks?slide=31

https://blog.innerht.ml/google-yolo/

https://www.sitepoint.com/common-pitfalls-avoid-using-html5-application-cache/

https://books.google.nl/books?id=jm3sEVZq8cIC&pg=PA392&lpg=PA392&dq=avoid+directly+serving+html&source=bl&ots=5ykQrUFUNk&sig=ACfU3U0LSfaIOp7ai798TFjA-pOTB2UbGA&hl=en&sa=X&ved=2ahUKEwjDluvP4bHnAhXQKVAKHRw8AYoQ6AEwCHoECGAQAQ#v=onepage&q=avoid%20directly%20serving%20html&f=false

https://perishablepress.com/stupid-htaccess-tricks/#sec1 

## Logging

### grafana + prometheus

https://prometheus.io/

https://grafana.com/

### Zabbbix

https://www.zabbix.com/

https://www.sans.org/white-papers/232/

https://www.cisecurity.org/controls/cis-controls-self-assessment-tool-cis-csat/`


### Traefik (https://traefik.io/)


(nginx proxy with auto letscencrypt)

### Logwatch (https://wiki.archlinux.org/title/Logwatch)

Logwatch is a powerful and versatile log parser and analyzer. Logwatch is designed to give a unified report of all activity on a server, which can be delivered through the command line or email. 

### Munin (https://munin-monitoring.org/)

Munin is a networked resource monitoring tool that can help analyze resource trends and "what just happened to kill our performance?" problems. It is designed to be very plug and play. A default installation provides a lot of graphs with almost no work.

### crowdsec (https://crowdsec.net/)

CrowdSec is a free, open-source and collaborative IPS.
Analyze behaviors, respond to attacks & share signals across the community.