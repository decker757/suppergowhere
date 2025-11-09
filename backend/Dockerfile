FROM golang:1.23-alpine AS build
WORKDIR /app
COPY go.mod .
RUN go mod download
COPY . .
# build main package (your main.go)
RUN CGO_ENABLED=0 GOOS=linux go build -o server .

FROM alpine:3.20
RUN adduser -D app
USER app
COPY --from=build /app/server /server
EXPOSE 4000
ENTRYPOINT ["/server", "-port=4000", "-env=development"]