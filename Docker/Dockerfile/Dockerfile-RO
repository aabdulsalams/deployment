FROM nginx:stable-alpine

# Essentials
RUN echo "UTC" > /etc/timezone
RUN apk add --no-cache nano

# Add certbot
RUN apk add --no-cache certbot certbot-nginx

# Change work directory
WORKDIR /etc/nginx

# Copy to docker
COPY ./etc/nginx/conf.d/router/nginx.conf /etc/nginx/nginx.conf
COPY ./etc/nginx/conf.d/router/common.conf /etc/nginx/common.conf
COPY ./etc/nginx/conf.d/router/common_location.conf /etc/nginx/common_location.conf
COPY ./etc/nginx/conf.d/router/ssl.conf /etc/nginx/ssl.conf