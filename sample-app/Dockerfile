FROM golang:1.21-alpine AS builder
WORKDIR /app
COPY . .
RUN go build -o app .

FROM alpine:3.19
COPY --from=builder /app/app .
EXPOSE 8080
CMD ["./app"]
