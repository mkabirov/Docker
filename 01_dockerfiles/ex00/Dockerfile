FROM alpine

RUN apk update && apk upgrade && apk add vim

ENTRYPOINT vim

# FROM specifies the base image. Dockerfiles must start with this or ARG
# RUN runs commands inside the image.
# ENTRYPOINT specifies the command that's run automatically

#first cd in the Dockerfile directory and build dockerfle :
#docker build -t ex00 .    
#run Dockerfile (ex00 - name):
#docker run --rm -ti ex00     
