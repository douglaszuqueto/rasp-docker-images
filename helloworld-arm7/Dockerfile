FROM douglaszuqueto/caddy-arm7

MAINTAINER Douglas Zuqueto <douglas.zuqueto@gmail.com>

COPY app/index.html /app/

EXPOSE 80

CMD ["/root/caddy", "-port", "80", "-conf", "/root/Caddyfile"]
