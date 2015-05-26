FROM phusion/baseimage:0.9.16

CMD ["/sbin/my_init"]

RUN apt-get update && apt-get install -y \
    build-essential \
    python-dev \
    python-pip \
    sudo \
    git \
    vim

RUN pip install --upgrade pip

RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
