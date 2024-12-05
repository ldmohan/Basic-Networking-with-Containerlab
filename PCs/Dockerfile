# The base image is Ubuntu 22.04 LTS ("jammy").
FROM ubuntu:22.04

# Variables to automatically install/update tzdata.
ARG DEBIAN_FRONTEND=noninteractive
ENV TZ=Europe/Berlin

# Update base image with new packages.
RUN apt update && apt dist-upgrade -y && apt autoremove -y && apt autoclean

# Install some basic tools and dependencies.
RUN apt install -y sudo nano bash net-tools ldnsutils iputils-ping traceroute iproute2 \
    xauth openssh-server tcpdump unzip subversion git curl wget gcc make perl g++ \
    software-properties-common libsctp-dev lksctp-tools libssl-dev ffmpeg
 
CMD ["bash"]



  