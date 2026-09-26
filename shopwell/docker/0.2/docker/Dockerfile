#syntax=docker/dockerfile:1.4

# pin versions
FROM ghcr.io/shopwell-shop/docker-base:8.3 AS base-image
FROM ghcr.io/shopwell-shop/shopwell-cli:latest-php-8.3 AS shopwell-cli

# build

FROM shopwell-cli AS build

ARG SHOPWELL_PACKAGES_TOKEN

ADD . /src
WORKDIR /src

ENV SHOPWELL_CACHE_ID=docker

RUN --mount=type=secret,id=composer_auth,dst=/src/auth.json \
    --mount=type=cache,target=/root/.composer \
    --mount=type=cache,target=/root/.npm \
    /usr/local/bin/entrypoint.sh shopwell-cli project ci /src

# build final image

FROM base-image

COPY --from=build --chown=82 --link /src /var/www/html
