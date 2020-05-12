FROM nvidia/cuda:9.0-cudnn7-devel-ubuntu16.04

RUN apt-get update && apt-get upgrade -y
RUN apt-get install -y build-essential checkinstall libreadline-gplv2-dev libncursesw5-dev libssl-dev libsqlite3-dev tk-dev libgdbm-dev libc6-dev libbz2-dev zlib1g-dev openssl libffi-dev wget nano python3 python3-pip

RUN wget https://download.pytorch.org/whl/cu100/torch-0.4.1-cp35-cp35m-linux_x86_64.whl

RUN pip3 install torch-0.4.1-cp35-cp35m-linux_x86_64.whl

WORKDIR /home
