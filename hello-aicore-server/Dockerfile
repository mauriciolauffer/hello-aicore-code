# Base layer (default dependencies) to use
# You should find more base layers at https://hub.docker.com
FROM python:3.13
ENV LANG C.UTF-8

# Custom location to place code files
RUN mkdir -p /app/src
COPY main.py requirements.txt /app/src/

# Required to execute script
RUN pip install -r /app/src/requirements.txt && \
    chgrp -R nogroup /app && \
    chmod -R 770 /app
