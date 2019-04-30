# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bgonzale <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/04/29 20:31:08 by bgonzale          #+#    #+#              #
#    Updated: 2019/04/29 20:48:24 by bgonzale         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM gcc
COPY . /usr/src/myapp
WORKDIR /usr/src/myapp
RUN gcc -o myapp main.c
CMD ["./myapp"]

# $ docker build -t myapp-c .
# buid Dockerfile
# $ docker run -it --rm --name my-c-app myapp-c
# run Dockerfile
# $ docker image rm --force $(docker images -a -q)
# removes all docker images that where build by Dockerfile
# ignore '$'
