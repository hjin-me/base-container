FROM rust:latest
RUN apt-get update && apt-get install -y librust-clang-sys-dev
RUN rustup toolchain install nightly
RUN rustup default nightly
RUN rustup target add wasm32-unknown-unknown
RUN cargo install --locked cargo-leptos
