---
layout: post
title: "Installing Docker and Portainer"
date: 2023-09-06 12:00:00 -0500
categories: [docker,portainer]
tags: [docker,portainer,linux,networking,] #all tags MUST be lowercase
image: https://marketplace-assets.digitalocean.com/logos/portaineriolimit-portainercommuni.svg
---

### TLDR
- Update system
``` 
sudo apt-get update
sudo apt-get upgrade
```
- Install and run Docker
```
sudo apt install docker.io
sudo systemctl enable docker
sudo systemctl start docker
sudo systemctl status docker
```
- Install and configure Portainer
```
sudo docker run -d \
--name="portainer" \
--restart on-failure \
-p 9000:9000 \
-p 8000:8000 \
-v /var/run/docker.sock:/var/run/docker.sock \
-v portainer_data:/data \
portainer/portainer-ce:latest
```