FROM ubuntu:20.04

RUN apt-get update && apt-get install -y python3 python3-pip sudo

RUN useradd -m sumanshu

RUN chown -R sumanshu:sumanshu /home/sumanshu

COPY ./requirements.txt /home/sumanshu/app/requirements.txt

COPY ./src /home/sumanshu/app/src

COPY ./model /home/sumanshu/app/model

COPY ./static /home/sumanshu/app/static

COPY ./templates /home/sumanshu/app/templates

COPY ./app.py /home/sumanshu/app/app.py

COPY ./Dockerfile /home/sumanshu/app/Dockerfile

USER sumanshu

RUN cd /home/sumanshu/app/ && pip3 install -r requirements.txt

WORKDIR /home/sumanshu/app