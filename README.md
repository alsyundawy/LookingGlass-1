# LookingGlass

## Overview

LookingGlass is a user-friendly PHP based looking glass that allows the public (via a web interface) to execute network
commands on behalf of your server.

Current version: v1.3.0

It's recommended that everyone updates their existing install!

## Features

* Automated install via bash script
* IPv4 & IPv6 support
* Live output via long polling
* Multiple themes
* Rate limiting of network commands

## Implemented commands

* host
* mtr
* mtr6 (IPv6)
* ping
* ping6 (IPv6)
* traceroute
* traceroute6 (IPv6)

__IPv6 commands will only work if your server has external IPv6 setup (or tunneled)__

## Requirements

* PHP >= 5.3
* PHP PDO with SQLite driver (required for rate-limit)
* SSH/Terminal access (able to install commands/functions if non-existent)

## Install

1. `git clone https://github.com/max2max/LookingGlass`
3. `cd LookingGlass/LookingGlass`
4. Run `bash configure.sh`
5. Follow the instructions and `configure.sh` will take care of the rest

`wget https://cdn.ipip.net/17mon/besttrace4linux.zip`<br />
`unzip besttrace4linux.zip`<br />
`chmod +x besttrace`<br />
`cp ./besttrace /usr/local/bin/`<br />
`echo "www ALL=(root)  NOPASSWD:/usr/local/bin/besttrace" >> /etc/sudoers`<br />

_Forgot a setting? Simply run the `configure.sh` script again_


## Apache

An .htaccess is included which protects the rate-limit database, disables indexes, and disables gzip on test files.
Ensure `AllowOverride` is on for .htaccess to take effect.

Output buffering __should__ work by default.

For an HTTPS setup, please visit:
- [Mozilla SSL Configuration Generator](https://mozilla.github.io/server-side-tls/ssl-config-generator/)

## Nginx

To enable output buffering, and disable gzip on test files please refer to the provided configuration:

[HTTP setup](LookingGlass/lookingglass-http.nginx.conf)

The provided config is setup for LookingGlass to be on a subdomain/domain root.

For an HTTPS setup please visit:
- [Best nginx configuration for security](http://tautt.com/best-nginx-configuration-for-security/)
- [Mozilla SSL Configuration Generator](https://mozilla.github.io/server-side-tls/ssl-config-generator/)

## License

Code is licensed under MIT Public License.

* If you wish to support my efforts, keep the "Powered by LookingGlass" link intact.
