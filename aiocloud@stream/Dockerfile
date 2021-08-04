FROM debian:buster-slim

RUN set -x; deps='wget curl unzip'  \
    &&  apt-get update  \
    &&  apt-get install -y $deps  \
    &&  curl -fsSL https://raw.githubusercontent.com/aiocloud/stream/master/scripts/kickstart.sh | bash  \
    &&  apt-get purge -y --auto-remove $deps  \

COPY stream.conf /etc/stream.conf

CMD stream