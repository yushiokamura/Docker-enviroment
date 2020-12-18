FROM continuumio/miniconda3:4.8.3

ENV http_proxy=""
ENV https_proxy=""

COPY . /home
WORKDIR /home


SHELL ["/bin/bash", "--login", "-c"]

RUN conda create -n miniconda-env python=3.8

SHELL ["conda", "run", "-n", "miniconda-env", "/bin/bash", "-c"]


RUN conda install pip
RUN pip install -r requirements.txt
ENV PYTHONPATH="/home:$PYTHONPATH"
RUN echo "conda activate honda" >> ~/.bashrc 

CMD jupyter lab --port 8000 --ip=0.0.0.0 --allow-root --NotebookApp.token=''
