build:
	apk add --no-cache go openssh
	export GOROOT=/usr/lib/go
	export GOPATH=/go
	export PATH=/go/bin:${PATH}
	mkdir -p ${GOPATH}/src ${GOPATH}/bin
	cp -r ../../. /app
	git config --global url.git@github.com:.insteadOf https://github.com/
	mkdir /root/.ssh && echo "StrictHostKeyChecking no " > /root/.ssh/config
	cd /app && CGO_ENABLED=0 GOOS=linux GOARCH=amd64 go build .
