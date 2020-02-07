FROM ubuntu
RUN apt-get update && \
	apt-get upgrade -y && \
	apt-get install -y python3.6 git vim
CMD bin/bash

# setting up Python enviroment
#build&run:
# docker build -t py .'
# docker run --rm -ti py'