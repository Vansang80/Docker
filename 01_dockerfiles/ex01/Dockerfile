FROM		debian:latest

RUN			apt-get update -y && apt-get upgrade -y && \
			apt-get install -qy wget tar bzip2 sudo && \
			rm -rf /var/cache/apt/* && \
			sudo adduser teamspeak --disabled-password --gecos ""  && \
			sudo su teamspeak && \
			wget http://dl.4players.de/ts/releases/3.0.11.2/teamspeak3-server_linux-amd64-3.0.11.2.tar.gz && \
			tar -zxvf teamspeak3-server_linux-amd64-3.0.11.2.tar.gz && \
			rm teamspeak3-server_linux-amd64-3.0.11.2.tar.gz

WORKDIR		/teamspeak3-server_linux-amd64

CMD			["sh", "ts3server_minimal_runscript.sh"]
