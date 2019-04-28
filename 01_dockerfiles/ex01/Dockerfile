# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bgonzale <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/04/27 17:55:47 by bgonzale          #+#    #+#              #
#    Updated: 2019/04/27 19:46:35 by bgonzale         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM debian

RUN apt-get update \
 && apt-get upgrade -y \
 && apt-get install wget bzip2 -y \
 && wget http://dl.4players.de/ts/releases/3.0.13.8/teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2 \
 && tar xfv teamspeak3-server_linux_amd64-3.0.13.8.tar.bz2

ENTRYPOINT ["sh", "teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh"]

# Sources:
# https://forum.teamspeak.com/threads/132611-Install-teamspeak-3-server-on-Debian-8

# Notes:
# $ docker build -t ex01 .
# build docker image with name ex01
# $ docker run -it --rm -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
# runs docker image ex01
# $ docker image rm --force $(docker images -a -q)
# removes all docker images that where build by Dockerfile
# $ docker images
# $ docker image ls
# list all docker images
# ignore '$'
