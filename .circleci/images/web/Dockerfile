
#Get the CircleCI base image
FROM cimg/base:stable-20.04 AS base

USER root
#Install Python
RUN apt-get update
#RUN apt-get install python3.8

#Install pip
RUN apt-get install python3-pip -y

#Install RabbitMQ
RUN apt-get install rabbitmq-server

#Install requirements
RUN wget https://raw.githubusercontent.com/GeekZoneHQ/web/master/requirements.txt
RUN pip3 install -r requirements.txt

#Run RabbitMQ
RUN systemctl enable rabbitmq-server

#Run a Celery worker
RUN celery -A web worker

