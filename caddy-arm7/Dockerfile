FROM douglaszuqueto/alpine-arm7

MAINTAINER Douglas Zuqueto <douglas.zuqueto@gmail.com>

COPY Caddyfile /root/

RUN apk update && \
    apk upgrade && \
    apk add --no-cache curl  && \
    cd ~ && \
    curl -o caddy.tar.gz "https://caddyserver.com/download/build?os=linux&arch=arm&arm=7&features=" && \
    tar -zxvf caddy.tar.gz && \
    apk del curl && rm -rf /var/cache/apk/* && rm -rf /var/lib/apt/lists/* && rm -rf caddy.tar.gz

EXPOSE 80

CMD ["/root/caddy", "-port", "80", "-conf", "/root/Caddyfile"]
