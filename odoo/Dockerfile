FROM ubuntu:18.04
MAINTAINER Ben <ben@chintech.com.cn>

ENV LANG C.UTF-8

COPY wkhtmltox_0.12.1.3-1~bionic_amd64.deb /opt
RUN set -x; \
            apt-get update \
            && apt-get upgrade -y\
            && apt-get install -y --no-install-recommends \
                python3-pip \
                build-essential \
                python3-dev \
                python3-venv \
                python3-wheel \
                libxslt-dev \
                libzip-dev \
                libldap2-dev \
                libsasl2-dev \
                python3-setuptools \
                vim \
                git \
                postgresql-client \
                fontconfig \
                /opt/wkhtmltox_0.12.1.3-1~bionic_amd64.deb \
            && rm -rf /var/lib/apt/lists/* \
            && rm -rf /opt/wkhtmltox_0.12.1.3-1~bionic_amd64.deb
RUN set -x; \
    git clone git@github.com:alreadytakenn/odoo.git /opt/odoo

RUN set -x; \
    pip3 install wheel \
    && pip3 install -r /opt/odoo/odoo/requirements.txt

