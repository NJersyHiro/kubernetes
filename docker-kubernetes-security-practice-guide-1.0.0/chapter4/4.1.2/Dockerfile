# syntax=docker/dockerfile:1.1-experimental
FROM ubuntu:18.04
RUN  apt-get update && apt-get install -y git openssh-client && \
  useradd -m -u 1000 exampleuser
USER exampleuser
RUN  mkdir -p -m 0700 ~/.ssh && \
  ssh-keyscan git.example.com >> ~/.ssh/known_hosts
RUN --mount=type=ssh,uid=1000 \
  git clone git@git.example.com/foo/bar.git
