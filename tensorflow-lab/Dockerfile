FROM tensorflow/tensorflow:2.0.0b0-gpu-py3 AS target-build

LABEL author="yashwanthremidi@gmail.com"

COPY requirements.txt requirements.txt
RUN pip3 install -r requirements.txt

RUN apt-get install nodejs -y && apt-get install npm -y 

COPY jupyter_notebook_config.py jupyter_notebook_config.py

RUN jupyter labextension install @jupyterlab/git && \
    jupyter labextension install @jupyterlab/google-drive && \
    jupyter labextension install @jupyterlab/vega4-extension && \
    jupyter labextension install @jupyterlab/plotly-extension && \
    jupyter labextension install @jupyterlab/geojson-extension && \
    jupyter labextension install jupyterlab-drawio && \
    jupyter labextension install @jupyterlab/latex && \
    jupyter labextension install @jupyterlab/github && \
    jupyter labextension install @oriolmirosa/jupyterlab_materialdarker && \
    jupyter labextension install @telamonian/theme-darcula


WORKDIR /project
EXPOSE 8888


CMD [ "jupyter", "lab", "--config", "/jupyter_notebook_config.py", "--no-browser", "--allow-root"]



