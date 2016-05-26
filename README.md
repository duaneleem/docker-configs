# docker-configs
The purpose of this repo is to provide a variety of Docker configurations for various web stacks I use for web development projects.

I hope a few of my Dockerfile templates may help you get started with your web projects.

Dockerfile: /nginx
I've had problems with NGINX refreshing web contents from my browser.  I've created this Dockerfile configuration to push an artifact (nginx.conf) to disable "sendfile on."  This problem stems from VirtualBox and NGINX.  To use this:

docker run --name container-name -p 8080:80 -v "/local/app/on/your/computer":"/usr/share/nginx/html":ro -d duaneleem/nginx:0.1

Don't use the following configuration Dockerfiles as they are currently being worked on:
/nginx-dev
