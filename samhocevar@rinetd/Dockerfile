FROM alpine:latest

RUN set -x; apk add --no-cache git automake autoconf gcc g++ make libffi-dev openssl-dev \
    && git clone https://github.com/samhocevar/rinetd.git \
    && cd rinetd \
    && ./bootstrap \
    && ./configure  \
    && make \
    && apk del git automake autoconf gcc g++ make libffi-dev openssl-dev \
    && chmod +x rinetd && cp rinetd /usr/bin/rinetd \
    && rm -rf * \

ENTRYPOINT rinetd -f
