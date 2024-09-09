# Use the official Alpine image as the base
FROM alpine:latest

# Install Postfix and other necessary packages
RUN apk update && \
    apk add --no-cache postfix bash

# Set up Postfix to run in the foreground
RUN echo "daemon_directory = /usr/lib/postfix/sbin" >> /etc/postfix/main.cf && \
    echo "compatibility_level = 2" >> /etc/postfix/main.cf && \
    sed -i 's/#daemon_directory/daemon_directory/' /etc/postfix/master.cf

# Expose the SMTP port
EXPOSE 25

# Set the command to start Postfix
CMD ["postfix", "start-fg"]
