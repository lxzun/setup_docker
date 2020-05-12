FROM nvidia/cuda:10.0-cudnn7-devel-ubuntu16.04

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y build-essential checkinstall libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev zlib1g-dev openssl libffi-dev wget nano

RUN mkdir /tmp/Python37
WORKDIR /tmp/Python37
RUN wget https://www.python.org/ftp/python/3.7.6/Python-3.7.6.tar.xz
RUN tar xvf Python-3.7.6.tar.xz
WORKDIR /tmp/Python37/Python-3.7.6
RUN ./configure --enable-optimizations
RUN make altinstall

WORKDIR /tmp/Python37
RUN wget https://download.pytorch.org/whl/cu100/torch-1.1.0-cp37-cp37m-linux_x86_64.whl

RUN pip3.7 install torch-1.1.0-cp37-cp37m-linux_x86_64.whl

WORKDIR /home
