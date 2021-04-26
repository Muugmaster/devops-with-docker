FROM golang:1.16.3-alpine3.13

EXPOSE 8080

WORKDIR /usr/src/app/

COPY . .

RUN addgroup -S appgroup && adduser -S appuser -G appgroup && go build

USER appuser

CMD ["go", "run", "server"]
