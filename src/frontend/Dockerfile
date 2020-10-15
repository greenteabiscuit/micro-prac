FROM golang:1.15

ENV HOME /root
ENV PATH $PATH:/usr/local/go/bin
ENV GOPATH /go 
RUN echo $GOPATH
RUN go get -u github.com/golang/protobuf/protoc-gen-go
RUN go get -u github.com/grpc-ecosystem/go-grpc-middleware/logging/zap
RUN go get -u go.uber.org/zap

WORKDIR /go/src/micro-sample-frontend
COPY . .

RUN go build -o /usr/local/bin/micro-sample-frontend

CMD ["micro-sample-frontend"]
