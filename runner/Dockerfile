FROM quay.io/podman/stable:v5

# Enable Podman socket
ENV DOCKER_HOST=unix:///run/podman/podman.sock
RUN systemctl enable --now podman.socket

# Install Forgejo Runner
ENV RUNNER_VERSION=12.3.1
RUN export ARCH=$(uname -m | sed 's/x86_64/amd64/;s/aarch64/arm64/') \
    && curl -o /bin/forgejo-runner "https://code.forgejo.org/forgejo/runner/releases/download/v${RUNNER_VERSION}/forgejo-runner-${RUNNER_VERSION}-linux-${ARCH}" \
    && chmod +x /bin/forgejo-runner

# Setup home directory
ENV HOME=/data
USER 1000:1000
VOLUME /data
WORKDIR /data

CMD ["/bin/forgejo-runner"]
