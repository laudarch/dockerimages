FROM alpine:3.1
MAINTAINER Beardyjay <jay@beardyjay.co.uk>

RUN apk add --update \
  bash \
  && rm -rf /var/cache/apk/*

# Install dnsrecon from git along with deps 
WORKDIR /usr/share
RUN echo 'bad stuff4' > /tmp/file

ENTRYPOINT ["/bin/bash"]
