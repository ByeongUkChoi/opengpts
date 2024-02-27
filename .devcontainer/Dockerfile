# Backend Dockerfile
FROM ubuntu:22.04
RUN apt update -y
RUN apt install software-properties-common -y
RUN add-apt-repository ppa:deadsnakes/ppa -y
RUN DEBIAN_FRONTEND=noninteractive TZ=Etc/UTC apt install python3 python3-pip -y

# Install system dependencies
RUN apt-get update && apt-get install -y libmagic1 && rm -rf /var/lib/apt/lists/*

# Set the working directory
WORKDIR /workspace

COPY . .

WORKDIR /workspace/backend

RUN rm poetry.lock

RUN pip install .