# Install Docker on Raspberry Pi

## Commands

```
curl -fsSL https://get.docker.com -o get-docker.sh
sh get-docker.sh

sudo groupadd docker
sudo usermod -aG docker $USER
newgrp docker
docker container run hello-world
```

## Ref

{% embed url="https://linuxize.com/post/how-to-install-and-use-docker-on-raspberry-pi/" %}

