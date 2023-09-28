FROM golang:1.21.1

WORKDIR /app

COPY ./golang/go.mod ./golang/go.sum ./

RUN go mod download

COPY ./golang/main.go ./

RUN CGO_ENABLED=0 GOOS=linux go build -o /hello-go

CMD [ "/hello-go" ]
EXPOSE 8080
