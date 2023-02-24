FROM centos:7

RUN yum -y update

RUN yum install -y centos-release-scl which && \
    yum groupinstall -y "Development Tools" && \
    yum install -y git gcc ca-certificates wget openssl-devel gnuplot perf vim && yum clean all

RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh -s -- -y
ENV PATH /root/.cargo/bin:$PATH

