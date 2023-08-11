FROM rust:latest
RUN apt-get install -y librust-clang-sys-dev
RUN rustup target add wasm32-unknown-unknown
RUN rustup toolchain install nightly
RUN rustup default nightly
RUN rustup target add wasm32-unknown-unknown
RUN cargo install dioxus-cli@0.3.2
COPY tools /root/.local/share/dioxus/tools
RUN chmod +x /root/.local/share/dioxus/tools/binaryen/bin/* /root/.local/share/dioxus/tools/tailwindcss/tailwindcss
