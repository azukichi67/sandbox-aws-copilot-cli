FROM ubuntu:24.10

RUN apt-get update && apt-get install -y \
    bash \
    curl \
    git \
    vim \
    zip \
    unzip \
    build-essential \
    && rm -rf /var/lib/apt/lists/*

RUN curl "https://awscli.amazonaws.com/awscli-exe-linux-x86_64.zip" -o "awscliv2.zip" && unzip awscliv2.zip && ./aws/install
RUN curl -Lo copilot https://github.com/aws/copilot-cli/releases/latest/download/copilot-linux && chmod +x copilot && mv copilot /usr/local/bin/copilot

WORKDIR /usr/src/app
CMD ["bash"]