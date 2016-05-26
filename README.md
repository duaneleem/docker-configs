# Docker Configurations

## Table of Contents
1. Dockerfile: /nginx
  * Docker build
  * Docker run
2. Test Dockerfiles (for test purposes)

The purpose of this repo is to provide a variety of Docker configurations for various web stacks I use for web development projects.   I hope a few of my Dockerfile templates may help you get started with your web projects.


## Dockerfile: /nginx

I've had problems with NGINX refreshing web contents from my browser.  I've created this Dockerfile configuration to push an artifact (nginx.conf) to disable "sendfile on."  This problem stems from VirtualBox and NGINX from my Google'ing sessions.  

**Build**: `docker build -t duaneleem/nginx:0.1 .`

To use this:

**Run**: ` docker run --name container-name -p 8080:80 -v "/local/app/on/your/computer":"/usr/share/nginx/html":ro -d duaneleem/nginx:0.1 `

Replace `/local/app/on/your/computer` with your local folder that has all your HTML files.  This will serve up your webpage on port 8080.


## Currently being worked on.

Don't use the following configuration Dockerfiles as they are currently being worked on:
/nginx-dev
