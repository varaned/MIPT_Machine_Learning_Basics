FROM ubuntu:24.04

RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install git htop iotop python3-pip mc 

WORKDIR /tmp

COPY requirements.txt ./

RUN rm -f /usr/lib/python3.12/EXTERNALLY-MANAGED

RUN pip3 install --no-cache-dir -r requirements.txt

CMD ["bash"]