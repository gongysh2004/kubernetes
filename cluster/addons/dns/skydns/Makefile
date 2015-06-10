all: skydns

skydns:
	CGO_ENABLED=0 go build -a -installsuffix cgo --ldflags '-w' github.com/skynetservices/skydns

container: skydns
	sudo docker build -t dockerreg.99cloud.net/google_containers/skydns .

push: container
	sudo docker push dockerreg.99cloud.net/google_containers/skydns

clean:
	rm -f skydns
