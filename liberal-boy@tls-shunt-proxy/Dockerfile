FROM alpine:latest

RUN set -x; apk add --no-cache unzip wget \
    && wget https://github.com/liberal-boy/tls-shunt-proxy/releases/download/0.7.0/tls-shunt-proxy-linux-amd64.zip \
    && unzip tls-shunt-proxy-linux-amd64.zip \
    && chmod +x tls-shunt-proxy && mv tls-shunt-proxy /usr/bin/tls-shunt-proxy \
    && apk del unzip wget \
    && rm -rf tls-shunt-proxy*

CMD tls-shunt-proxy
