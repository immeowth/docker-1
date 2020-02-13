FROM debian

WORKDIR /home/teamspeak

EXPOSE 9987/udp 30033 10011

RUN apt-get update && apt-get upgrade -y && apt-get install -y wget bzip2

RUN wget https://files.teamspeak-services.com/releases/server/3.10.2/teamspeak3-server_linux_amd64-3.10.2.tar.bz2 && \
	tar -xvf teamspeak3-server_linux_amd64-3.10.2.tar.bz2

WORKDIR teamspeak3-server_linux_amd64

RUN touch .ts3server_license_accepted

ENTRYPOINT ./ts3server_startscript.sh start
