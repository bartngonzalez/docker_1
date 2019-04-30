# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bgonzale <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/04/29 20:02:37 by bgonzale          #+#    #+#              #
#    Updated: 2019/04/29 20:07:06 by bgonzale         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ubuntu

RUN apt-get update \
 && apt-get install --no-install-recommends build-essential ca-certificates -y \
 && apt-get install nginx -y \
 && apt-get install git -y \
 && apt-get install mariadb-server mariadb-client -y \
 && apt-get install golang-go -y \
 && apt-get install wget -y \
 && service mysql start \
 && echo 'export GOPATH=$HOME/go' >> $HOME/.bashrc \
 && go get -u github.com/gogs/gogs \
 && cd /root/go/src/github.com/gogs/gogs && go build -v -tags 'sqlite'

ENV USER="root"
WORKDIR /root/go/src/github.com/gogs/gogs
EXPOSE 3000:3000
EXPOSE 22:22
USER root
CMD ["./gogs", "web"]

# Notes:
# $ docker build -t ex03 .
# build Dockerfile
# $ docker run -p 3000:3000 -p 32:32 --name testgit ex03
# select SQLite3 && run user "root"
# $ docker image rm --force $(docker images -a -q)
# removes all docker images that where build by Dockerfile
# ignore '$'
