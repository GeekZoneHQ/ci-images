
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

#Copy requirements.txt into container
COPY requirements.txt .

#Install requirements
RUN pip3 install -r requirements.txt

