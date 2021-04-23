FROM alpine:latest

RUN set -x; apk add --no-cache wget tar \
    && wget https://github.com/shadowsocks/shadowsocks-rust/releases/download/v1.10.8/shadowsocks-v1.10.8.x86_64-unknown-linux-musl.tar.xz \
    && tar -xvJf shadowsocks-v1.10.8.x86_64-unknown-linux-musl.tar.xz \
    && chmod +x ss* \
    && mv ss* /usr/bin/ \
    && rm -rf shadowsocks* \
    && apk del wget tar
