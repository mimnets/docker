FROM ubuntu

ENV TZ=Asia/Dhaka \
    DEBIAN_FRONTEND=noninteractive \
    LANG=en_US.UTF-8 \
    LC_ALL=en_US.UTF-8

RUN apt-get update && apt-get install -y \
    python3 python3-pip python3-venv \
    python3-setuptools python3-dev build-essential \
    default-libmysqlclient-dev locales tzdata curl git && \
    ln -fs /usr/share/zoneinfo/$TZ /etc/localtime && \
    dpkg-reconfigure -f noninteractive tzdata && \
    locale-gen en_US.UTF-8

WORKDIR /opt

COPY app.py /opt/app.py

RUN python3 -m venv venv && \
    /opt/venv/bin/pip install --upgrade pip && \
    /opt/venv/bin/pip install flask

EXPOSE 5000

CMD ["/opt/venv/bin/python", "/opt/app.py"]
