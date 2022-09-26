# syntax=docker/dockerfile:1

# Using Golang base images
# Contains all the base tools and dependency to run a go application
FROM golang:1.17-alpine

WORKDIR /app

COPY go.* ./

RUN go mod download

COPY . ./

# Creates a binary file of our app which will be used to serve the application
RUN  go build main.go

EXPOSE 3000

CMD [ "go","run","main.go" ]

