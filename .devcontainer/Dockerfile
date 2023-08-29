FROM mcr.microsoft.com/devcontainers/cpp:1-ubuntu-22.04

# From oot/Dockerfile
RUN ln -snf /usr/share/zoneinfo/$TZ /etc/localtime && echo $TZ > /etc/timezone && \
    apt-get update && \
    apt-get install -y \
        binutils-mips-linux-gnu \
        build-essential \
        pkg-config \
        python3 \
        python3-pip \
        git \
        wget \
        unzip \
        clang-tidy \
        clang-format \
        libpng-dev && \
    apt-get clean && \
    rm -rf /var/lib/apt/lists/*

RUN python3 -m pip install --user colorama ansiwrap attrs watchdog python-Levenshtein "mapfile-parser>=1.2.1,<2.0.0" "rabbitizer>=1.0.0,<2.0.0"
RUN python3 -m pip install --upgrade attrs pycparser

ENV LANG C.UTF-8

# [Optional] Uncomment this section to install additional vcpkg ports.
# RUN su vscode -c "${VCPKG_ROOT}/vcpkg install <your-port-name-here>"

# [Optional] Uncomment this section to install additional packages.
# RUN apt-get update && export DEBIAN_FRONTEND=noninteractive \
#     && apt-get -y install --no-install-recommends <your-package-list-here>
