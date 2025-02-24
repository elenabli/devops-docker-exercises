FROM golang:1.16

WORKDIR /app

COPY . .

RUN go build -o server

RUN go test ./...

ENV PORT=8080
ENV REQUEST_ORIGIN=http://example.com

EXPOSE 8080

CMD ["./server"]