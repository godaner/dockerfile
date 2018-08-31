FROM centos
WORKDIR /usr/local/go/src
ENV GOPATH=/usr/local/go
ENV GOBIN=/usr/local/go/bin
ENV email=""
ENV emailPassword=""
ENV emailHost=""
ENV emailPort=0
RUN yum install -y golang && \
	yum install -y git && \
	git clone https://github.com/godaner/wxautoreplyrobot.git
WORKDIR /usr/local/go/src/wxautoreplyrobot/cmd
CMD go run main.go -textReplyPath /usr/local/go/src/wxautoreplyrobot/textreply.cfg -addr :8887 -email $email -emailPassword $emailPassword -emailHost $emailHost -emailPort $emailPort
	
