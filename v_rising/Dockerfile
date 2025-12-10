FROM ghcr.io/parkervcp/steamcmd:proton

ENV SRCDS_APPID=1829350
ENV STARTUP="proton run ./VRisingServer.exe -persistentDataPath data"

RUN usermod -u 1000 -g 1000 container

VOLUME /home/container
EXPOSE 9876-9877/udp
