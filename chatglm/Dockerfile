FROM python
COPY . /app
WORKDIR /app
RUN apt update && apt install -y cmake vim
RUN pip install -r requirements.txt