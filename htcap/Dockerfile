FROM python:2
MAINTAINER Beardyjay <jay@beardyjay.co.uk>

WORKDIR /root
RUN apt-get update
RUN apt-get -y install build-essential g++ flex bison gperf ruby perl sqlite3 python

# Install phantomJS
RUN wget https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2
RUN tar xvjf phantomjs-2.1.1-linux-x86_64.tar.bz2
RUN mv /root/phantomjs-2.1.1-linux-x86_64/bin/phantomjs /usr/bin/phantomjs

# Install SQLMap
WORKDIR /root/
RUN git clone https://github.com/sqlmapproject/sqlmap.git sqlmap-dev

# Install HTCAP
WORKDIR /usr/share
RUN git clone https://github.com/segment-srl/htcap.git
RUN ln -s /usr/share/htcap/htcap.py /usr/local/bin/htcap
RUN ln -s /usr/share/htcap/scripts/htmlreport.py /usr/local/bin/htcap_report
RUN ln -s /usr/share/htcap/scripts/quickscan.sh /usr/local/bin/htcapquick

WORKDIR /root
ENTRYPOINT ["/bin/bash"]
