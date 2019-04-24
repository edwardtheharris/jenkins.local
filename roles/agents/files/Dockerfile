FROM jenkins/jnlp-slave:alpine
USER root
RUN apk add python3 py3-pip build-base alpine-sdk openssl-dev libffi-dev
RUN apk add libxml2-dev libxslt-dev
RUN apk add python3-dev
WORKDIR /opt
RUN git clone https://github.com/ansible/ansible
WORKDIR /opt/ansible
RUN pip3 install --upgrade pip
RUN pip3 install ansible/
RUN pip3 install ansible-lint
RUN pip3 install beancount beancount-plugins fava
RUN mkdir -p /etc/ansible
COPY hosts /etc/ansible/hosts
