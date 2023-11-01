FROM golang:latest AS builder
WORKDIR /app
COPY main.go .
RUN go mod init main/app
RUN go build main.go


FROM scratch
COPY --from=builder /app . 
CMD ["./main"]

