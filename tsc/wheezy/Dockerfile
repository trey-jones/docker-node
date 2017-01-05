FROM node:wheezy
MAINTAINER Trey Jones "trey@eyesoreinc.com"

RUN npm install -g typescript@~1.6
RUN mkdir /tsc
WORKDIR /tsc

ENTRYPOINT ["tsc"]
