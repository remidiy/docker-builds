FROM tensorflow/tensorflow:2.0.0b0-gpu-py3 AS target-build

LABEL author="yashwanthremidi@gmail.com"

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

RUN apt-get install nodejs -y && apt-get install npm -y 

COPY jupyter_notebook_config.py jupyter_notebook_config.py
COPY jupyter_settings/.jupyter .jupyter
WORKDIR /project

EXPOSE 8888

CMD [ "jupyter", "lab", "--no-browser", "--allow-root"]



