# Start with Ubuntu base image
FROM ubuntu:14.04
MAINTAINER Kai Arulkumaran <design@kaixhin.com>

# Install LXDE, VNC server and Firefox
RUN apt-get update && DEBIAN_FRONTEND=noninteractive apt-get install -y \
  firefox \
  lxde-core \
  lxterminal \
  tightvncserver
# Set user for VNC server (cannot use USER)
ENV USER root
# Set default password
COPY password.txt .
RUN cat password.txt password.txt | vncpasswd
RUN rm password.txt
# Expose VNC port
EXPOSE 5901

# Run VNC server with tail in the foreground
CMD vncserver :1 -geometry 1280x800 -depth 24 && tail -F /root/.vnc/*.log