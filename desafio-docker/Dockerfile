FROM golang:alpine3.11 AS builder

WORKDIR /app

COPY ./hello.go .

RUN go build -o main .

FROM scratch

COPY --from=builder /app/main/ .

ENTRYPOINT ["./main"]
