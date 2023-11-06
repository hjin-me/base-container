FROM ubuntu:22.04
ENV TZ Asia/Shanghai
ENV LANG zh_CN.utf8
RUN ln -fs /usr/share/zoneinfo/Asia/Shanghai /etc/localtime;
RUN set -ex; \
	apt-get update; \
	DEBIAN_FRONTEND=noninteractive apt-get install -y --no-install-recommends \
        wget \
        language-pack-zh-hans \
	    tzdata \
	    ca-certificates; \
    apt-get clean;
RUN /usr/share/locales/install-language-pack zh_CN


RUN wget https://dl.google.com/linux/direct/google-chrome-stable_current_amd64.deb &&\
    apt update -y &&\
    apt install ./google-chrome-stable_current_amd64.deb -y &&\
    rm -rf ./google-chrome-stable_current_amd64.deb &&\
    apt-get clean;
ENV CHROME /usr/bin/google-chrome
