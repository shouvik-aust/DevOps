# Class 2

## Using NGINX in Container & Modifying HTML Landing page

NGINX is open source software for web serving, reverse proxying, caching, load balancing, media streaming, and more. In addition to its HTTP server capabilities, NGINX can also function as a proxy server for email (IMAP, POP3, and SMTP) and a reverse proxy and load balancer for HTTP, TCP, and UDP servers.

[I am using EC2 instance from AWS to install & use docker]

### Step:1 - Prepare a customized HTML File & name it as 'index.html'

### Step:2 - Prepare Docker File
`FROM ubuntu` <br>
`RUN apt update` <br>
`RUN apt install nginx -y` <br>
`COPY ./index.html /var/www/html` : */var/www/html* This is the default path that the Nginx uses as the default <br> 
`CMD ["nginx", "-g","daemon off;"]`

### Step: 3 - Build & Run Docker Image

1. `sudo docker build -t shouvik/nginx-custom2 .`: builds the docker file 
2. `sudo docker run -p 80:80 shouvik/nginx-custom2` : runs the docker file & creates a container, *The container shall start to run* 


My hosted HTML page can be seen [HERE.](http://18.139.161.212/)
