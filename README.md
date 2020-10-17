# docker
docker images
---
Docker and Docker-compose installation
-
curl -fsSL https://get.docker.com -o get-docker.sh<br>
sudo sh get-docker.sh<br>
sudo curl -L "https://github.com/docker/compose/releases/download/1.24.1/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose<br>
sudo chmod +x /usr/local/bin/docker-compose<br>
sudo ln -s /usr/local/bin/docker-compose /usr/bin/docker-compose<br>
docker-compose --version<br>
