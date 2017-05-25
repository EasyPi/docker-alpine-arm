.PHONY: build test push clean

build: qemu-arm-static
	docker build -t easypi/alpine-arm:build .

test:
	docker run --rm easypi/alpine-arm:build uname -a

push:
	docker push easypi/alpine-arm:build

qemu-arm-static:
	wget -O- https://github.com/multiarch/qemu-user-static/releases/download/v2.8.4/qemu-arm-static.tar.gz | tar xz

clean:
	rm -f qemu-arm-static
