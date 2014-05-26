altoids-websites-docker
======================

This repository contains the docker image that will host my websites.
This is intented to be used with [altoids](https://github.com/eljojo/altoids).

### How to build?

As usual, ``docker build -t altoids-websites .`` will do the trick.

### How to run?

The image is expecting the websites to be mountes as volumes.

Currently this image is hosting:
- eljojo.net
- ajipirijou.com

They need to be mounted under ``/var/www/[domain.tld]``

The image can be started as following:

```
docker run -p 80:80 -v /eljojo.net:/var/www/eljojo.net:ro altoids-websites
```

