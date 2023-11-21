FROM rust:latest
RUN apt-get update && apt-get install -y librust-clang-sys-dev musl-tools
RUN rustup toolchain install nightly
RUN rustup default nightly
RUN rustup target add wasm32-unknown-unknown
RUN rustup target add x86_64-unknown-linux-musl
RUN cargo install --git https://github.com/DioxusLabs/dioxus dioxus-cli
# install tailwindcss
RUN mkdir -p /root/.local/share/dioxus/tools/tailwindcss \
    && wget https://github.com/tailwindlabs/tailwindcss/releases/download/v3.3.5/tailwindcss-linux-x64 -O /root/.local/share/dioxus/tools/tailwindcss/tailwindcss \
    && chmod +x /root/.local/share/dioxus/tools/tailwindcss/tailwindcss
# install binaryen
RUN mkdir -p /root/.local/share/dioxus/tools/binaryen \
    && wget https://github.com/WebAssembly/binaryen/releases/download/version_116/binaryen-version_116-x86_64-linux.tar.gz -O ./binaryen.tar.gz \
    && tar -xzf binaryen.tar.gz -C /root/.local/share/dioxus/tools/binaryen --strip-components=1 \
    && rm binaryen.tar.gz && chmod +x /root/.local/share/dioxus/tools/binaryen/bin/*