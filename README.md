# Dante SOCKS Proxy

This is an open proxy docker image, you should use it with a gateway to control access.

## Test the proxy by asking it to download google.com
`replace 127.0.0.1 with the ip/hostname`
```shell 
curl -v -x socks5://127.0.0.1:2020 http://www.google.com/
```

## Run the proxy
```shell
docker run -p 2020:2020 lthn/dante
```
## Build with Composer
```shell
docker compose up
```
## Compose service
```yaml
version: '3'
services:
  sockd:
    build:
      dockerfile: Dockerfile
    restart: always
    ports:
      - "2020:2020"
```