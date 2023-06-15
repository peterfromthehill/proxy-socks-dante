# Dante SOCKS Proxy

This is a docker image configured to provide SOCKSv5 access to a VPN node,
using pam to auth with auth.host.uk.com 

```shell
docker compose up
```

# Test the proxy by asking it to download google.com

```shell 
curl -v -x socks5://sockd:sockd@127.0.0.1:2020 http://www.google.com/
```