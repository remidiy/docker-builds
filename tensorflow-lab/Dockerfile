FROM tensorflow/tensorflow:2.0.0b0-gpu-py3 AS target-build

LABEL author="yashwanthremidi@gmail.com"

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

COPY jupyter_notebook_config.py jupyter_notebook_config.py
WORKDIR /project

EXPOSE 8888

RUN apt-get install nodejs -y && apt-get install npm -y 

CMD [ "jupyter", "lab", "--config", "/jupyter_notebook_config.py", "--no-browser", "--allow-root"]



