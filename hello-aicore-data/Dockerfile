# Specify which base layers (default dependencies) to use
# You may find more base layers at https://hub.docker.com/
FROM python:3.13

# Creates directory within your Docker image
# Don't place anything in below folders yet, just create them
RUN mkdir -p /app/src/ && \
    mkdir -p /app/data/ && \
    mkdir -p /app/model/

# Copies file from your Local system TO path in Docker image
COPY main.py requirements.txt /app/src/

# Installs dependencies within you Docker image
# Enable permission to execute anything inside the folder app
RUN pip install -r /app/src/requirements.txt && \
    chgrp -R 65534 /app && \
    chmod -R 777 /app
