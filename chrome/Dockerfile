FROM ubuntu:22.04
RUN set -ex; \
	apt-get update; \
	apt-get install -y --no-install-recommends \
        wget \
	    tzdata \
	    locales \
	    ca-certificates; \
    apt-get clean;
RUN locale-gen zh_CN.UTF-8; \
    update-locale zh_CN.UTF-8;
RUN cp /usr/share/zoneinfo/Asia/Shanghai /etc/localtime;
ENV TZ Asia/Shanghai
ENV LANG zh_US.utf8

RUN wget https://dl.google.com/linux/direct/google-chrome-beta_current_amd64.deb &&\
    apt update -y &&\
    apt install ./google-chrome-beta_current_amd64.deb -y &&\
    rm -rf ./google-chrome-beta_current_amd64.deb &&\
    apt-get clean;
ENV CHROME /usr/bin/google-chrome
