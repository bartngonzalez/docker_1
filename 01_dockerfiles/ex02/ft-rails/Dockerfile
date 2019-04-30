# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bgonzale <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/04/28 18:18:01 by bgonzale          #+#    #+#              #
#    Updated: 2019/04/29 16:35:24 by bgonzale         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM ruby:2.5.1

RUN apt-get update \
 && apt-get install -y nodejs=4.8.2~dfsg-1 \
 && rm -rf /var/lib/apt/lists/* \
 && gem install rails bundler

ONBUILD COPY app /opt/app
ONBUILD WORKDIR /opt/app

ONBUILD RUN bundler install
ONBUILD RUN rails db:migrate
ONBUILD RUN rails db:seed

# Notes:
# $ docker build -t ft-rails:on-build .
# this creates the Dockerfile from the subjeuct
# $ docker build -t ex02 .
# this is to build the Dockerfile in the root of the folder
# $ docker run -it -p 3000:3000 --rm ex02
# this runs the built image
# $ docker image rm --force $(docker images -a -q)
# removes all docker images that where build by Dockerfile
# ignore '$'
