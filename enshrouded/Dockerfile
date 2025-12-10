FROM ghcr.io/parkervcp/steamcmd:proton

ENV SRCDS_APPID=2278520
ENV STARTUP="rm ./logs/enshrouded_server.log && proton run ./enshrouded_server.exe & PID=\$! && tail -c0 -F ./logs/enshrouded_server.log --pid=\$PID"

RUN usermod -u 1000 -g 1000 container

VOLUME /home/container
EXPOSE 15636-15637/tcp
EXPOSE 15636-15637/udp
