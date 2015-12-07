FROM node:onbuild
MAINTAINER Matti Jokitulppo <matti.jokitulppo@aalto.fi>

RUN echo "deb http://archive.ubuntu.com/ubuntu precise main universe" > /etc/apt/sources.list
RUN apt-get update
RUN apt-get install curl
RUN apt-get upgrade -y

RUN npm install -g babel-cli

RUN curl -SL https://github.com/melonmanchan/sardroid-server/tarball/master \
    | tar -zxC /sardroid --strip-components=1

ADD . /sardroid

WORKDIR /sardroid

RUN npm install

EXPOSE 9001

CMD ["bash", "start-sardroid.sh"]
