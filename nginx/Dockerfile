FROM nginx:alpine

MAINTAINER Andrew Branch "andrew@wheream.io"

WORKDIR /etc/nginx

# Copy server configuration and sites
COPY gertybox-server /etc/nginx
RUN envsubst '\$UPTIME_PORT' < sites-available/uptime.wheream.io > sites-available/uptime.wheream.io

# Make and link sites_enabled  
RUN ln -s sites-available sites-enabled

