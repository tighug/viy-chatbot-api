FROM nvidia/cuda:11.7.0-runtime-ubuntu22.04

ENV TZ=Asia/Tokyo
ENV DEBIAN_FRONTEND=noninteractive
RUN apt-get update && apt-get install -y --no-install-recommends \
    build-essential \
    bat \
    curl \
    exa \
    git \
    python3-distutils \
    software-properties-common \
    tzdata \
    vim \
    zsh
RUN sh -c "$(curl -fsSL https://starship.rs/install.sh)" -y -f
RUN echo 'eval "$(starship init bash)"' >> ~/.bashrc
RUN apt-get autoremove -y
RUN curl -sSL https://raw.githubusercontent.com/python-poetry/poetry/master/get-poetry.py | python3 -