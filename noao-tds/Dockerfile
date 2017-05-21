FROM continuumio/anaconda3:4.3.1 
LABEL maintainer "maria.t.patterson@gmail.com"
ENV REFRESHED_AT 2017-05-19

ENV PATH="~/anaconda3/bin:$PATH"


RUN apt-get install -y libeigen3-dev gcc 
RUN /opt/conda/bin/conda config --add channels http://ssb.stsci.edu/astroconda 
RUN ["/bin/bash", "-c", "conda create -n astroconda stsci"]
RUN ["/bin/bash", "-c", "source activate astroconda"]
RUN ["/bin/bash", "-c", "conda install -c mpi4py openmpi=2.0.2"]

RUN apt-get install -y g++
ADD requirements.txt .
RUN pip install -r requirements.txt

