FROM rust:latest
RUN apt update && apt install -y librust-clang-sys-dev musl-tools && apt clean
RUN rustup toolchain install nightly
RUN rustup default nightly
RUN rustup target add wasm32-unknown-unknown
RUN rustup target add x86_64-unknown-linux-musl
RUN cargo install dioxus-cli@0.3.2
COPY tools /root/.local/share/dioxus/tools
RUN chmod +x /root/.local/share/dioxus/tools/binaryen/bin/* /root/.local/share/dioxus/tools/tailwindcss/tailwindcss
