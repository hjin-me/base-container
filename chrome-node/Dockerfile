FROM node:20
RUN wget https://dl.google.com/linux/direct/google-chrome-beta_current_amd64.deb &&\
    apt update -y &&\
    apt install ./google-chrome-beta_current_amd64.deb -y &&\
    rm -rf ./google-chrome-beta_current_amd64.deb
ENV PUPPETEER_EXECUTABLE_PATH /usr/bin/google-chrome
