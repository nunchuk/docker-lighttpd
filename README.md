<img src="https://raw.githubusercontent.com/nunchuk/docker-lighttpd/master/logo.png" width="100" />

# Lighttpd Docker image

This Docker image is based on [aliyun-alpine](https://github.com/nunchuk/aliyun-alpine).

## Quick start

```
docker run --name lighttpd -d \
	-p <http-port>:80 \
	-v <home-directory>:/var/www/localhost/htdocs \
	nunchuk/lighttpd
```

## Docker Compose start

Add the following lines in an `docker-compose.yml` file:

	lighttpd:
	  image: nunchuk/lighttpd
	  volumes:
	    - <home-directory>:/var/www/localhost/htdocs
	  ports:
	    - "<http-port>:80"

Then start a lighttpd container with:

```
docker-compose up lighttpd
```

Contributors
-------------------
* XinYe (nunchuk@live.com)