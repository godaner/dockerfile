FROM centos
WORKDIR /usr/local/go/src
ENV GOPATH=/usr/local/go
ENV GOBIN=/usr/local/go/bin
RUN yum install -y golang
RUN yum install -y git
RUN go get github.com/beego/bee
RUN git clone https://github.com/godaner/go-chat.git
WORKDIR /usr/local/go/src/go-chat
CMD /usr/local/go/bin/bee run
	