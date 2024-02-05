# cocker  インストール方法

https://docs.docker.com/engine/install/ubuntu/  より

sudo apt-get update
sudo apt-get install ca-certificates curl

sudo install -m 0755 -d /etc/apt/keyrings

sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

sudo chmod a+r /etc/apt/keyrings/docker.asc

echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null

  sudo apt-get update


  sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


 # docker compose
 DOCKER_CONFIG=${DOCKER_CONFIG:-$HOME/.docker}
 sudo mkdir -p $DOCKER_CONFIG/cli-plugins
 sudo curl -SL https://github.com/docker/compose/releases/download/v2.4.1/docker-compose-linux-x86_64 -o $DOCKER_CONFIG/cli-plugins/docker-compose

 sudo chmod +x $DOCKER_CONFIG/cli-plugins/docker-compose