FROM alpine:latest
MAINTAINER Trey Jones "trey@eyesoreinc.com"

RUN apk update && apk add nodejs && rm -rf /var/cache/apk/*

# after 1.6 tsc drops support for polling which is the only way for filewatching to work in docker
# support should be there to enable polling in a future release
RUN npm install -g typescript@~2.0
RUN mkdir /tsc
WORKDIR /tsc

ENTRYPOINT ["tsc"]
