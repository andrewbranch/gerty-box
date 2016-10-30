FROM nginx:1

MAINTAINER Andrew Branch "andrew@wheream.io"

WORKDIR /etc/nginx

# Copy server configuration and sites
COPY . /etc/nginx
RUN envsubst '\$UPTIME_PORT' < /etc/nginx/sites-available/uptime.wheream.io > /etc/nginx/sites-available/uptime.wheream.io

# Make and link sites_enabled  
RUN ln -s sites-available sites-enabled

