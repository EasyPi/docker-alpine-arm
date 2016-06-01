docker-alpine-arm
=================

![](https://badge.imagelayers.io/easypi/alpine-arm:latest.svg)

Build AlpineLinuxArm Docker Image for RaspberryPi.

## How To Build

```bash
docker login

wget https://raw.githubusercontent.com/EasyPi/docker-alpine-arm/master/Makefile

make RELEASE=edge
make test RELEASE=edge
make push RELEASE=edge
make clean

make RELEASE=v3.4
make test RELEASE=v3.4
make push RELEASE=v3.4
make clean

make latest RELEASE=v3.4
make test RELEASE=latest
make push RELEASE=latest
```

## How To Use

```bash
docker pull easypi/alpine-arm
docker run --rm -it easypi/alpine-arm sh
# apk update
# apk search bash
# apk add bash
# apk del bash
# exit
```
