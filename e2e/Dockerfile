FROM golang:1.14-alpine3.11

RUN apk add --no-cache \
  openssl

ENV CGO_ENABLED=0

COPY . /go/src/github.com/carrotsong/dtls
WORKDIR /go/src/github.com/carrotsong/dtls/e2e

CMD ["go", "test", "-tags=openssl", "-v", "."]
