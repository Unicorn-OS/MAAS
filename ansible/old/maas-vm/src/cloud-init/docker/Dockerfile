FROM ubuntu:18.04
RUN apt update
RUN apt install -y cloud-image-utils
COPY . /app

# add to path
RUN ln -sr /app/seed /usr/bin/

ENTRYPOINT seed
