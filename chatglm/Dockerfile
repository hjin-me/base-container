#FROM python
#FROM pytorch/pytorch:1.4-cuda10.1-cudnn7-runtime
#FROM pytorch/pytorch:2.0.0-cuda11.7-cudnn8-devel
FROM pytorch/pytorch:2.0.0-cuda11.7-cudnn8-runtime
COPY . /app
WORKDIR /app
RUN apt update && apt install -y cmake vim
RUN pip install -r requirements.txt \
    && find /usr/local/lib/ -name '*.pyc' -delete