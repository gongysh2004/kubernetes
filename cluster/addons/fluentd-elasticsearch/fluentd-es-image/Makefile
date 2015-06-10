.PHONY:	build push

IMAGE = fluentd-elasticsearch
TAG = 1.5

build:	
	sudo docker build -t dockerreg.99cloud.net/google_containers/$(IMAGE):$(TAG) .

push: build	
	suod docker push dockerreg.99cloud.net/google_containers/$(IMAGE):$(TAG)
