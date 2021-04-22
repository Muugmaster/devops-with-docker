FROM golang:alpine AS builder

RUN apk update && apk add --no-cache git
WORKDIR $GOPATH/src/mypackage/myapp/
COPY . .

RUN go get -d -v

RUN go build -o /go/bin/server

FROM scratch

COPY --from=builder /go/bin/server /go/bin/server

ENTRYPOINT ["/go/bin/server"]
CMD ["go", "run", "server"]