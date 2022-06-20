FROM raspbian/stretch:latest

WORKDIR /opt/app

RUN apt-get update && \
    apt-get upgrade -y && \
    apt-get install -y --no-install-recommends \
    vim python3 python3-pip git\
    && apt-get -y clean \
    && rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install --upgrade pip
RUN python3 -m pip install RPi.GPIO

RUN git clone https://github.com/Alicey0719/DHT11_Post.git

ENTRYPOINT [ "tail", "-f", "/dev/null" ] 