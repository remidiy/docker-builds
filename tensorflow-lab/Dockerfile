FROM tensorflow/tensorflow:2.0.0b0-gpu-py3 AS target-build

LABEL author="yashwanthremidi@gmail.com"

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

RUN apt-get install nodejs -y && apt-get install npm -y 

COPY jupyter_notebook_config.py jupyter_notebook_config.py

RUN jupyter labextension install @jupyterlab/git \
    @jupyterlab/google-drive \
    @jupyterlab/vega4-extension \
    @jupyterlab/plotly-extension \
    @jupyterlab/geojson-extension \
    jupyterlab-drawio \
    @jupyterlab/latex \
    @jupyterlab/github \
    @oriolmirosa/jupyterlab_materialdarker \
    @telamonian/theme-darcula


WORKDIR /project
EXPOSE 8888


CMD [ "jupyter", "lab", "--config", "/jupyter_notebook_config.py", "--no-browser", "--allow-root"]



