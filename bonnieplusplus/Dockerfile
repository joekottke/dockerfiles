FROM alpine:3.7
MAINTAINER Joe Kottke <joe.kottke@gmail.com>

ENV BONNIE_VERSION=1.97.3 \

RUN \
  apk add --no-cache --virtual .build-deps g++ make perl wget openssl && \
  cd /tmp && wget https://www.coker.com.au/bonnie++/bonnie++-${BONNIE_VERSION}.tgz && \
  tar xvf bonnie++-${BONNIE_VERSION}.tgz && cd bonnie++-${BONNIE_VERSION}/ && \
  ./configure && make && make install && \
  rm /tmp/bonnie++-${BONNIE_VERSION}.tgz && \
  rm -r /tmp/bonnie++-${BONNIE_VERSION}/

CMD ['/usr/local/sbin/bonnie++']

