FROM jupyter/pyspark-notebook:latest

COPY . /home
WORKDIR /home

RUN pip install jupyterlab

ENV PYSPARK_PYTHON=/opt/conda/bin/python
ENV PYSPARK_DRIVER_PYTHON=/opt/conda/bin/jupyter
ENV PYSPARK_DRIVER_PYTHON_OPTS="lab --port 8888 --ip=0.0.0.0 --allow-root --NotebookApp.token=''"

CMD pyspark