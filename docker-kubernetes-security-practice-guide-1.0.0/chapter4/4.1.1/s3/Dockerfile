# syntax=docker/dockerfile:1.1-experimental
FROM ubuntu:18.04
RUN  apt-get update && apt-get install -y awscli && \
  useradd -m -u 1000 exampleuser
USER exampleuser
RUN mkdir -p /home/exampleuser/.aws
RUN  --mount=type=secret,id=aws,target=/home/exampleuser/.aws/credentials,uid=1000 \
 aws s3 cp s3://examplebucket/exampleobject .
