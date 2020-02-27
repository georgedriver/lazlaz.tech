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

## Setup http proxy \[optional\]

```text
$ mkdir -p /etc/systemd/system/docker.service.d
$ nano /etc/systemd/system/docker.service.d/http-proxy.conf
$ cat /etc/systemd/system/docker.service.d/https-proxy.conf
[Service]
Environment=”HTTP_PROXY=http://<proxy_server>:<port>"
#Environment=”HTTPS_PROXY=https://<proxy_server>:<port>"
$ sudo systemctl daemon-reload
$ sudo systemctl restart docker
```

## Ref

{% embed url="https://linuxize.com/post/how-to-install-and-use-docker-on-raspberry-pi/" %}

