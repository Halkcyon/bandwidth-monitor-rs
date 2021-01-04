# https://github.com/microsoft/vscode-dev-containers/tree/v0.154.0/containers/rust/.devcontainer/base.Dockerfile
FROM mcr.microsoft.com/vscode/devcontainers/rust:0-1

RUN apt-get update \
    && export DEBIAN_FRONTEND=noninteractive \
    && apt-get -y upgrade \
    && apt-get -y install --no-install-recommends libdbus-1-dev

RUN rustup default nightly \
    && rustup component add rustfmt clippy rust-src

RUN cargo install --all-features cargo-add starship bat ripgrep
