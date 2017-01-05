FROM mhart/alpine-node:latest
MAINTAINER Trey Jones "trey@eyesoreinc.com"

RUN apk add --update --no-cache python python-dev make gcc g++ automake autoconf linux-headers

# install watchman
RUN mkdir -p /build/watchman/
ADD https://github.com/facebook/watchman/archive/v4.7.0.zip     /build/watchman
RUN cd /build/watchman && \
    unzip v4.7.0.zip && \
    cd watchman-4.7.0 && \
    ./autogen.sh && \
    ./configure && \
    make && \
    make install

RUN npm i angular-cli@1.0.0-beta.24 -g

RUN apk del python-dev automake autoconf linux-headers

RUN mkdir /ng
VOLUME /ng
WORKDIR /ng

ENTRYPOINT ["ng"]
