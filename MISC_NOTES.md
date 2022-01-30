# Miscellaneous notes

## NGINX

*I am curious why you use an ingress-nginx deployment. It looks like your blog pod is also running a nginx container, which makes sense. You could just point cloudflared at the service of that pod could you not?*

https://kubernetes.github.io/ingress-nginx/deploy/

*It's unfortunate that there aren't better solutions for securely exposing a part of your home network to the cloud. Imagine if it were easy to set up a secure solution to access your home lab from anywhere - you could use it as your own private cloud. And perhaps then it would also be easy to expose part of that publicly, like a blog.*

- Wireguard.

- https://www.cloudflare.com/products/tunnel/


## Webdeb debugging

https://christianheilmann.com/2021/11/01/developer-tools-secrets-that-shouldnt-be-secrets/