# Securing Linux servers.



Turn on SELinux
Security-Enhanced Linux (SELinux) is an access control security mechanism provided in the kernel.

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



For extra security https://www.cyberciti.biz/tips/linux-security.html


## Web security.

https://speakerdeck.com/filedescriptor/exploiting-the-unexploitable-with-lesser-known-browser-tricks?slide=31

https://blog.innerht.ml/google-yolo/

https://www.sitepoint.com/common-pitfalls-avoid-using-html5-application-cache/

https://books.google.nl/books?id=jm3sEVZq8cIC&pg=PA392&lpg=PA392&dq=avoid+directly+serving+html&source=bl&ots=5ykQrUFUNk&sig=ACfU3U0LSfaIOp7ai798TFjA-pOTB2UbGA&hl=en&sa=X&ved=2ahUKEwjDluvP4bHnAhXQKVAKHRw8AYoQ6AEwCHoECGAQAQ#v=onepage&q=avoid%20directly%20serving%20html&f=false

https://perishablepress.com/stupid-htaccess-tricks/#sec1  