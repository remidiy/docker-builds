FROM nvidia/cuda:10.0-base

MAINTAINER remidi "yashwanthremidi@gmail.com"

RUN apt-get update -y
RUN apt-get upgrade -y
RUN apt-get install -y python3-pip build-essential
RUN apt-get install -y git 
RUN apt-get install -y cmake zlib1g-dev libjpeg-dev xvfb libav-tools xorg-dev python-opengl libboost-all-dev libsdl2-dev swig


COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt