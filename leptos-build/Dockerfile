FROM node:lts
RUN apt-get update && apt-get install -y librust-clang-sys-dev
RUN curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
RUN rustup toolchain install stable
RUN rustup default stable
RUN rustup target add wasm32-unknown-unknown
# RUN cargo install --locked cargo-leptos
RUN cargo install --git https://github.com/leptos-rs/cargo-leptos --locked cargo-leptos
COPY ./ssr_modes /ssr_modes
RUN cd /ssr_modes && cargo leptos build --release && cd .. && rm -rf /ssr_modes
