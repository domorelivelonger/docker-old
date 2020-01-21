# pptpd-docker-alpine
Minimal docker Alpine image with PPTPD VPN.

### Usage
```
git clone https://github.com/0dataexpert0/pptpd-docker-alpine.git
cd pptpd-docker-alpine
docker-compose up -d
```
or with Docker build
```
git clone https://github.com/0dataexpert0/pptpd-docker-alpine.git
cd pptpd-docker-alpine
docker build .
docker images
docker run --name pptpd -d --restart=always   --publish 1723:1723   \
--volume ./chap-secrets:/etc/ppp/chap-secrets   \
paste_here_docker_image_id
```
When accessing the vpn, pptp user will be ```x```, and password will be ```x```
You can change it in file "chap-secrets", after restart container.

License
----

BSD
### Docker and Docker-compose installation
```
curl -fsSL https://get.docker.com -o get-docker.sh
sudo sh get-docker.sh
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
sudo chmod +x /usr/local/bin/docker-compose
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose
docker-compose --version
```
