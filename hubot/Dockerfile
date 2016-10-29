FROM node:argon

MAINTAINER Andrew Branch "andrew@wheream.io"

# Create directories on container
RUN mkdir -p /var/www
WORKDIR /var/www

# Copy app from host to container
RUN mkdir -p /var/tmp
COPY gerty/package.json /var/tmp/
RUN cd /var/tmp && npm install
COPY gerty .
RUN mv /var/tmp/node_modules ./
COPY .env .env

# Start the app
CMD ["bin/hubot", "-a", "slack"]
