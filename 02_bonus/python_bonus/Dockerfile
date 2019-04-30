# **************************************************************************** #
#                                                                              #
#                                                         :::      ::::::::    #
#    Dockerfile                                         :+:      :+:    :+:    #
#                                                     +:+ +:+         +:+      #
#    By: bgonzale <marvin@42.fr>                    +#+  +:+       +#+         #
#                                                 +#+#+#+#+#+   +#+            #
#    Created: 2019/04/29 20:41:57 by bgonzale          #+#    #+#              #
#    Updated: 2019/04/29 20:50:42 by bgonzale         ###   ########.fr        #
#                                                                              #
# **************************************************************************** #

FROM python:3

WORKDIR /usr/src/app

# COPY requirements.txt ./
# RUN pip install --no-cache-dir -r requirements.txt

COPY . .

CMD [ "python", "./hello.py" ]

# Notes:
# $ docker build -t myapp-python .
# build Dockerfile
# $ docker run -it --rm --name my-python-app myapp-python
# run Dockerfile
# $ docker image rm --force $(docker images -a -q)
# removes all docker images that where build by Dockerfile
# ignore '$'
