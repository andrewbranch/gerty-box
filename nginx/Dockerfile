FROM nginx:alpine

MAINTAINER Andrew Branch "andrew@wheream.io"

WORKDIR /etc/nginx
ARG UPTIME_PORT
ARG GERTY_PORT

# Copy server configuration and sites
COPY gertybox-server /etc/nginx
RUN mkdir sites-available && \
    envsubst '\$GERTY_PORT' < gerty.wheream.io.template > sites-available/gerty.wheream.io

# Make and link sites_enabled  
RUN ln -s sites-available sites-enabled

