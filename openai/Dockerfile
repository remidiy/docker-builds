FROM tensorflow/tensorflow:2.0.0a0-gpu-py3

MAINTAINER remidi "yashwanthremidi@gmail.com"

RUN apt-get update -y && apt-get install -y git

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

WORKDIR /workdir