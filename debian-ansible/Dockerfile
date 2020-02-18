FROM debian:buster
LABEL maintainer="oborde@henix.fr" Description="Debian 10 for ansible use" tag="buster"

RUN apt update
RUN apt install -y openssh-server python3 python3-pip
RUN mkdir -p /root/.ssh
COPY id_rsa.pub /root/.ssh/authorized_keys
# Add your ssh public key id_rsa.pub before bulding docker image