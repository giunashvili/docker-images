FROM ubuntu:20.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update 
RUN apt-get install curl python3-distutils python3.8 openssh-client -y
RUN curl https://bootstrap.pypa.io/get-pip.py | python3.8

RUN pip install ansible-core==2.13
RUN pip install boto3 botocore 

RUN ansible-galaxy collection install amazon.aws && \
    ansible-galaxy collection install community.general && \
    ansible-galaxy collection install kubernetes.core && \
    ansible-galaxy collection install community.mysql