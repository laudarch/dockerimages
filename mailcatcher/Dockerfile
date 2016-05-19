FROM alpine:3.2
MAINTAINER Jay Scott <jay@beardyjay.co.uk>

RUN apk update && apk upgrade && apk add \
    ruby \
    g++ \
    musl-dev \
    make \
    ruby-dev \
    sqlite-dev \
    bash \
    && rm -rf /var/cache/apk/*

RUN gem install mailcatcher --no-ri --no-rdoc

EXPOSE 1025
EXPOSE 1080

CMD ["mailcatcher", "-f", "--ip=0.0.0.0"]
