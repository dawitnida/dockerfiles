FROM golang:alpine
MAINTAINER Jessica Frazelle <jess@linux.com>

RUN	apk add --no-cache \
	bash \
	ca-certificates \
	curl \
	gcc \
	git \
	jq \
	make \
	musl-dev

RUN go get github.com/golang/lint/golint
RUN go get honnef.co/go/tools/cmd/staticcheck
# TODO: remove this eventually
RUN go get golang.org/x/crypto/ssh/terminal

COPY upload-assets /usr/bin/upload-assets
COPY release-email-notification /usr/bin/release-email-notification
COPY gcloud-login /usr/bin/gcloud-login
