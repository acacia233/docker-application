FROM debian:buster-slim

RUN set -x; deps='wget curl unzip'  \
    &&  apt-get update  \
    &&  apt-get install -y $deps  \
    &&  curl -fsSL https://raw.githubusercontent.com/aiocloud/stream/master/scripts/kickstart.sh | bash > /dev/null  \
    &&  apt-get purge -y --auto-remove $deps

CMD stream