FROM ubuntu:latest

RUN apt-get update && apt-get install -y \
    x11-apps \
    xvfb \
    && rm -rf /var/lib/apt/lists/*

ENV DISPLAY=:99

CMD Xvfb :99 -screen 0 1024x768x24 -ac +extension GLX +render -noreset & \
    sleep 5 && \
    DISPLAY=:99 xeyes

    