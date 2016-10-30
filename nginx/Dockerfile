FROM nginx:alpine

MAINTAINER Andrew Branch "andrew@wheream.io"

WORKDIR /etc/nginx

# Copy server configuration and sites
COPY gertybox-server /etc/nginx
RUN mkdir sites-available && \
    envsubst '\$UPTIME_PORT' < uptime.wheream.io.template > sites-available/uptime.wheream.io

# Make and link sites_enabled  
RUN ln -s sites-available sites-enabled

