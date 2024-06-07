FROM ubuntu:jammy

ARG VERSION
ENV VERSION=${VERSION}

RUN apt-get update && \
    apt-get install -y curl && \
    curl -L https://github.com/hasura/graphql-engine/raw/stable/cli/get.sh | bash

EXPOSE 9695