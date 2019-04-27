# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bgonzale <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/04/27 03:27:18 by bgonzale          #+#    #+#              #
#    Updated: 2019/04/27 04:33:16 by bgonzale         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM alpine:3.7

RUN apk update \
 && apk upgrade \
 && apk add --no-cache vim

ENTRYPOINT ["vim"]

# Notes:
# $ docker build --help
# list of build commands
# $ docker build -t ex00 .
# builds Dockerfile with name ex00
# $ docker run -it --rm ex00
# runs Dockerfile build ex00
# $ docker image rm --force $(docker images -a -q)
# removes all docker images that where build by Dockerfile
# ignore '$'
