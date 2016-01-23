# Nginx Image

## ImageLayer
* [![](https://badge.imagelayers.io/xataz/nginx:latest.svg)](https://imagelayers.io/?images=xataz/nginx:latest 'Get your own badge on imagelayers.io')

## Tag available
* latest, 1.9, 1.9.9 [(Dockerfile)](https://github.com/xataz/dockerfiles/blob/master/nginx/1.9.9/Dockerfile)

## Description
What is [Nginx](http://nginx.org)?

nginx (engine x) is an HTTP and reverse proxy server, a mail proxy server, and a generic TCP proxy server, originally written by Igor Sysoev. For a long time, it has been running on many heavily loaded Russian sites including Yandex, Mail.Ru, VK, and Rambler. According to Netcraft, nginx served or proxied 24.29% busiest sites in December 2015. Here are some of the success stories: Netflix, Wordpress.com, FastMail.FM.

## Build Image

```shell
docker build -t xataz/nginx github.com/xataz/dockerfiles.git#master:nginx/1.9.9
```

## Configuration
### Environments
* UID : Choose uid for launch 0bin (default : 991)
* GID : Choose gid for launch 0bin (default : 991)

### Volumes
* /www : Place your site's files here
* /sites-enabled : Place your vhost here
* /conf.d : If necessary, place configuration file here

### Ports
* 80
* 443

## Usage
### Advanced launch
```shell
docker run -d \
	-p 80:80 \
	-p 443:443 \
	-v /docker/config/nginx/www:/www \
	-v /docker/config/nginx/sites-enabled:/sites-enabled \
	xataz/nginx:1.9.9
```
