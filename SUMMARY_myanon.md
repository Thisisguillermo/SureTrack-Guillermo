https://www.linuxuprising.com/2018/10/how-to-install-and-use-tor-as-proxy-in.html

`sudo apt install apt-transport-https curl`

```
sudo -i

echo "deb https://deb.torproject.org/torproject.org/ $(lsb_release -cs) main" > /etc/apt/sources.list.d/tor.list

curl https://deb.torproject.org/torproject.org/A3C4F0F979CAA22CDBA8F512EE8CBC9E886DDD89.asc | gpg --import

gpg --export A3C4F0F979CAA22CDBA8F512EE8CBC9E886DDD89 | apt-key add -

apt update

exit
```

`sudo apt install tor tor-geoipdb torsocks deb.torproject.org-keyring`

`sudo apt install privoxy`

`sudo systemctl start privoxy`

`sudo vim /etc/privoxy/config`

And add this to the etc/privoxy/config file. (With the dot.)

```
forward-socks5 / localhost:9050 .
```

`sudo systemctl restart privoxy`

### Using Tor and Privoxy in Ubuntu or Linux Mint.

Using Tor via torsocks

To easily launch an application and make it use Tor, you can use torsocks, which works with both GUI and command line programs. This library ensures that DNS requests are handled safely and explicitly rejects any traffic other than TCP from the application you're using.

For example, to launch Spotify with torsocks, use:

`torsocks spotify`

`sudo apt install curl`

To test it, run this command to get your real IP address:

To check for your real IP address use:

`curl ipv4.icanhazip.com`

There is a problem with torsocks though - it fails to launch some applications. For example, running torsocks firefox or torsocks google-chrome does nothing. For such cases, you'll need to enter the Tor SOCKS5 proxy manually in the application you want to use - see below.

### Use a SOCKS5 proxy where possible or, if the application doesn't support it, use a regular HTTP proxy instead.

You can also use Tor as a system-wide proxy. For example in Gnome go to System Settings > Network, click on Network Proxy, set the proxy to Manual, then use localhost as the Socks Host and 9050 as the port:

*Note that Chromium-based web browsers (Google Chrome, Opera, Vivaldi, etc.) don't allow setting a proxy in their settings and instead use the system-wide proxy.*

`sudo systemctl reload tor`

### How to configure Tor to use country specific exit nodes (choose from which country your new IP should be)

`sudo vim /etc/tor/torrc`

Add the following two lines to the file, without changing anything else:

```
ExitNodes {COUNTRY_CODE}
StrictNodes 1
```

Replace COUNTRY_CODE with the 2 letter ISO3166 country code, for example use us for the United States, de for Germany, and so on. You can find a list of country codes here.

https://en.wikipedia.org/wiki/ISO_3166-1_alpha-2

`sudo systemctl reload tor`


### Use Socks proxy for B-Suite.

1. Under Project Options.
2. SOCKS proxy.
3. Enable "Use SOCKS Proxy"
4. Enable "Do DNS lookups over SOCKS PROXY"

127.0.0.1

9050