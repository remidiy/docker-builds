FROM nvidia/cuda:10.0-base

MAINTAINER remidi "yashwanthremidi@gmail.com"

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y python3-pip build-essentials

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt