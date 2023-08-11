FROM rust:latest
RUN curl -fsSL https://deb.nodesource.com/setup_18.x | bash -
RUN apt-get install -y nodejs librust-clang-sys-dev
RUN rustup target add wasm32-unknown-unknown
RUN cargo install dioxus-cli@0.3.2
COPY tools /root/.local/share/dioxus/tools
