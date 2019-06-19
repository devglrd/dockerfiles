FROM python:3.6

MAINTAINER "Gregoire MAHE <greg@asforge.com>"

RUN apt-get update

RUN apt-get install git && apt-get install nano

RUN pip3 install python-openstackclient python-designateclient

CMD openstack