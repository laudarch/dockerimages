FROM ruby:2.1.7
MAINTAINER Beardyjay <jay@beardyjay.co.uk>

# install deps for metasploit
WORKDIR /root
RUN apt-get update && apt-get -y install \
  build-essential \
  libreadline-dev \
  libssl-dev \
  libpq5 \
  libpq-dev \
  libreadline5 \
  libsqlite3-dev \
  libpcap-dev \
  git-core \
  autoconf \
  curl \
  zlib1g-dev \
  zlib1g \ 
  libxml2 \
  libxml2-dev \
  libxslt1-dev \
  locate \
  vncviewer \
  libyaml-dev \
&& rm -rf /var/lib/apt/lists/*

# get latest nmap and metasploit
RUN git clone https://github.com/nmap/nmap.git && git clone https://github.com/rapid7/metasploit-framework.git

# build and install nmap
WORKDIR /root/nmap
RUN ./configure && make && make install && make clean

# build Metasploit
WORKDIR /root/metasploit-framework
RUN bundle install

CMD ["./msfconsole"]
