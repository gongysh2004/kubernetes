# Makefile for the Docker image gcr.io/google_containers/kube2sky
# MAINTAINER: Tim Hockin <thockin@google.com>
# If you update this image please bump the tag value before pushing.

.PHONY: all kube2sky container push clean test

TAG = 1.9
PREFIX = dockerreg.99cloud.net/google_containers

all: container

kube2sky: kube2sky.go
	GOOS=linux GOARCH=amd64 CGO_ENABLED=0 godep go build -a -installsuffix cgo --ldflags '-w' ./kube2sky.go

container: kube2sky
	sudo docker build -t $(PREFIX)/kube2sky:$(TAG) .

push: kube2sky container
	sudo  docker push $(PREFIX)/kube2sky:$(TAG)

clean:
	rm -f kube2sky

test: clean
	godep go test -v --vmodule=*=4
