FROM debian

RUN apt-get update && apt-get upgrade -y && apt-get install -y wget bzip2 && \
wget http://dl.4players.de/ts/releases/3.8.0/teamspeak3-server_linux_amd64-3.8.0.tar.bz2 && \
tar -xvf teamspeak3-server_linux_amd64-3.8.0.tar.bz2

ENV TS3SERVER_LICENSE=accept

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh


#https://hub.docker.com/_/teamspeak - how to download

# RUN standard commands to download  &&
# download teamspeak3-server from their website &&
# extract the file we just downloaded

# ENV TS3SERVER_LICENSE=accept a licence 

# WORKDIR create a folder where we keep the unziped file &specify the work folder

# ENTRYPOINT specifies the command that's run automatically

# cd ex01 and build dockerfile
#docker build -t ex01 .
# run:
#docker run --rm -it -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
#to check from clinet side - download client from website teamspeak.com
#connect using Char IP