FROM ubuntu:latest

ENV DEBIAN_FRONTEND=noninteractive

WORKDIR /honeypots

COPY config.json /honeypots

RUN apt-get update

RUN apt-get install -y python3 python3-pip

RUN pip3 install honeypots

CMD [ "python3", "-m", "honeypots", "--setup", "all","--config", "config.json" ]