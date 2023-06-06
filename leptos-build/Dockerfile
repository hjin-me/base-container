FROM rust:latest
RUN apt-get update && apt-get install -y librust-clang-sys-dev
RUN rustup toolchain install nightly
RUN rustup default nightly
RUN rustup target add wasm32-unknown-unknown
RUN #cargo install --locked cargo-leptos
RUN cargo install --git https://github.com/leptos-rs/cargo-leptos --locked cargo-leptos
COPY ./ssr_modes /ssr_modes
RUN cd /ssr_modes && cargo leptos build --release && cd .. && rm -rf /ssr_modes
