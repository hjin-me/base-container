#FROM python
FROM pytorch/pytorch:2.0.1-cuda11.7-cudnn8-runtime
COPY . /app
WORKDIR /app
RUN apt update && apt install -y build-essential vim wget
RUN pip install -r requirements.txt \
    && find /usr/local/lib/ -name '*.pyc' -delete