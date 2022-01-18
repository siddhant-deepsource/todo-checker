build:
	apk add --no-cache go
	export GOROOT=/usr/lib/go
	export GOPATH=/go
	export PATH=/go/bin:${PATH}
	mkdir -p ${GOPATH}/src ${GOPATH}/bin
	cp -r ../../. /app
	cd /app && go build .
