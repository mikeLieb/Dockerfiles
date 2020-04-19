FROM debian

LABEL maintainer=@mlieb

ARG DEBIAN_FRONTEND=noninteracvtive

RUN /bin/bash -c 'source $HOME/.bashrc ;\
echo $HOME'

RUN apt-get update --fix-missing && \
	apt-get install -y \
	wget bzip2 ca-certificates \
	libglib2.0-0 libxext6 libsm6 libxrender1

RUN wget --quiet https://repo.anaconda.com/miniconda/Miniconda2-4.5.11-Linux-x86_64.sh -O ~/miniconda.sh && \
    /bin/bash ~/miniconda.sh -b -p /opt/conda && \
    rm ~/miniconda.sh
