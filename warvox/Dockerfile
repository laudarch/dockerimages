FROM debian:latest
MAINTAINER Jay Scott <jay@beardyjay.co.uk>

RUN apt-get update && apt-get -y install \
  gnuplot \
  lame \
  build-essential \
  libssl-dev \
  libcurl4-openssl-dev \ 
  postgresql-contrib \
  git-core \
  curl \
  libpq-dev \
  ruby2.1 \
  bundler \
  && rm -rf /var/lib/apt/lists/*

WORKDIR /home/warvox
RUN git clone git://github.com/rapid7/warvox.git /home/warvox \
    && ln -s /usr/bin/ruby2.1 /usr/bin/ruby \
    && git checkout c25db678ded165b56d64d94bddd23d98e6f97e0e \
    && bundle install \
    && make

ADD setup.sh /
EXPOSE 7777

CMD ["/setup.sh"]
