FROM debian:jessie
MAINTAINER beardyjay <jay@beardyjay.co.uk>

RUN apt-get update && apt-get -y install \
  asterisk \
  mpg123 \
  && rm -rf /var/lib/apt/lists/*


COPY *.conf /etc/asterisk/
COPY modem.wav /usr/share/asterisk/sounds/en/
EXPOSE 4569

CMD /usr/sbin/asterisk -f -U asterisk -G asterisk -vvvg -c
