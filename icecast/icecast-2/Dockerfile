FROM        ubuntu:20.04

LABEL       author="Softwarenoob" maintainer="admin@softwarenoob.com"

ENV         DEBIAN_FRONTEND noninteractive
# Install Dependencies
RUN         dpkg --add-architecture i386 
RUN         apt-get update 
RUN         apt-get upgrade -y 
RUN         apt-get install -y tar curl gcc g++ libgcc1 libcurl4-gnutls-dev:i386 libcurl4:i386 libtinfo5:i386 lib32z1 lib32stdc++6 libncurses5:i386 libcurl3-gnutls:i386 iproute2 gdb libsdl1.2debian libfontconfig telnet net-tools netcat tzdata icecast2
RUN         useradd -m -d /home/container container

USER        container
ENV         HOME /home/container
WORKDIR     /home/container

COPY        ./entrypoint.sh /entrypoint.sh
CMD         ["/bin/bash", "/entrypoint.sh"]
