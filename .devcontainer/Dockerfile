FROM ubuntu:24.04

RUN apt-get -y update && apt-get -y upgrade
RUN apt-get -y install git htop iotop python3-pip mc 

WORKDIR /tmp

COPY requirements.txt ./

RUN rm -f /usr/lib/python3.12/EXTERNALLY-MANAGED

RUN pip3 install --no-cache-dir -r requirements.txt

RUN CMAKE_ARGS='-DGGML_CUDA=on -DCMAKE_CUDA_ARCHITECTURES="89;120"' pip install llama-cpp-python --force-reinstall --verbose

CMD ["bash"]