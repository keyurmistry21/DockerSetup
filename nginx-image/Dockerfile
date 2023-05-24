FROM ubuntu:18.04
LABEL maintainer="keyur1ved@gmail.com"
RUN  apt-get -y update && apt-get -y install nginx
COPY files/default /etc/nginx/sites-available/default
COPY files/index.html /usr/share/nginx/html/index.html
EXPOSE 80
CMD ["/usr/sbin/nginx", "-g", "daemon off;"]

#FROM golang:1.18 as build
#WORKDIR /go/src/app
#COPY . .
#RUN go mod download
#RUN go vet -v
#RUN go test -v
#RUN CGO_ENABLED=0 go build -o /go/bin/app
#FROM gcr.io/distroless/static-debian11
#COPY --from=build /go/bin/app /
#CMD ["/app"]
