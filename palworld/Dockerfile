FROM ghcr.io/parkervcp/steamcmd:debian

ENV SRCDS_APPID=2394010
ENV STARTUP="./PalServer.sh -EpicApp=Palserver -useperfthreads -NoAsyncLoadingThread -UseMultithreadForDS"

RUN usermod -u 1000 -g 1000 container

VOLUME /home/container
EXPOSE 8211/udp
