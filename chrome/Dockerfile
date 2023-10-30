FROM debian:bullseye
RUN wget https://dl.google.com/linux/direct/google-chrome-beta_current_amd64.deb &&\
    apt update -y &&\
    apt install ./google-chrome-beta_current_amd64.deb -y &&\
    rm -rf ./google-chrome-beta_current_amd64.deb
ENV CHROME /usr/bin/google-chrome
