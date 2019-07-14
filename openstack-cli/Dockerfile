FROM python:3.6

RUN apt-get update && apt-get install --no-install-recommends --assume-yes nano=2.7.4-1 \
 && apt-get clean \
 && rm -rf /var/lib/apt/lists/*

RUN pip3 install python-openstackclient==3.19.0 python-designateclient==2.11.0

CMD ["openstack"]
