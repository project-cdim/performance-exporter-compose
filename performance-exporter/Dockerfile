FROM golang:1.24-alpine3.22

# upgrading packages
RUN apk update && \
    apk upgrade --available && \
    apk add --no-cache \
    curl

WORKDIR /app/logger
COPY ./performance-exporter/performance-exporter/logger/go.mod ./
COPY ./performance-exporter/performance-exporter/logger/go.sum ./
RUN go mod download

WORKDIR /app
COPY ./performance-exporter/performance-exporter/go.mod ./
COPY ./performance-exporter/performance-exporter/go.sum ./
RUN go mod download

# go build and exec
COPY performance-exporter/performance-exporter .
RUN go build -o /performance-exporter
CMD [ "/performance-exporter" ]
