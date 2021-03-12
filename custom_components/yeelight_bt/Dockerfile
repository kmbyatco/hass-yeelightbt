FROM python:3.8-slim

RUN apt-get update && apt-get install --no-install-recommends -y \
    build-essential \
    bluez \
    python-pip \
    libglib2.0-dev && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /opt/yeelight_bt
COPY . /opt/yeelight_bt

RUN pip install -r requirements.txt

CMD python3 -u /opt/yeelight_bt/yeelightbt.py
