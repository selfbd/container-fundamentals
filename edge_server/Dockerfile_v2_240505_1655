FROM alpine:3.16
LABEL org.opencontainers.image.authors="bds_uplimit@fastmail.fm"
LABEL org.opencontainers.image.server_type="edge_server"
RUN apk update
RUN apk add --no-cache nginx
COPY config/nginx.conf /etc/nginx/
COPY web_content/ /var/www
RUN rm -rf /var/cache/apk/*
EXPOSE 80
CMD ["nginx", "-g", "daemon off;"]
