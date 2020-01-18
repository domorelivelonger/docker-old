# danted-docker-alpine
Minimal docker Alpine image with socks5 proxy Danted.

### Usage
```
git clone https://github.com/domorelivelonger/danted-alpine.git
cd danted-alpine
docker-compose up -d
```
or with Docker build
```
git clone https://github.com/domorelivelonger/danted-alpine.git
cd danted-alpine
docker build .
docker images
docker run --name danted -d --restart=always   --publish 1080:1080   \
--volume ./sockd.conf:/etc/sockd.conf   \
paste_here_docker_image_id
```
When accessing the proxy, user will be ```x```, and password will be ```x```
You can change it
```
docker exec -ti danted sh
add Your_User
passwd Your_User
```
after restart container.

License
----

BSD
----


Usage
---
Configuring a SOCKS proxy server in Chrome
https://www.chromium.org/developers/design-documents/network-stack/socks-proxy
___
for Firefox use "FoxyProxy Standard"
https://addons.mozilla.org/en-US/firefox/addon/foxyproxy-standard/
___
![alt text](https://github.com/0dataexpert0/danted-docker-alpine/blob/master/03cbb8127509b3141c058ff37e195a97.jpg)
___
### Docker and Docker-compose installation
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
docker-compose --version
```
