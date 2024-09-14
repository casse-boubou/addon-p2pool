ARG BUILD_FROM=ghcr.io/hassio-addons/debian-base:7.5.0

# https://github.com/hassio-addons/addon-base/releases
# hadolint ignore=DL3006
FROM ${BUILD_FROM}

# https://github.com/eikek/sharry/releases
ARG P2POOL_VERSION=v4.1

# Add p2pool
RUN set -eux \
    apt-get update; \
    \
    mkdir -p /opt; \
    curl -s -J -L -o /tmp/p2pool.tar.gz \
        "https://github.com/SChernykh/p2pool/releases/download/${P2POOL_VERSION}/p2pool-${P2POOL_VERSION}-linux-aarch64.tar.gz"; \
    tar -xzf /tmp/p2pool.tar.gz -C /tmp; \
    mv /tmp/p2pool-${P2POOL_VERSION}-linux-aarch64/p2pool /opt/p2pool; \
    rm /tmp/p2pool.tar.gz; \
    rm -r /tmp/p2pool-${P2POOL_VERSION}-linux-aarch64
    
COPY --chmod=445 rootfs /
WORKDIR /

# Build arguments
ARG BUILD_ARCH
ARG BUILD_DATE
ARG BUILD_DESCRIPTION
ARG BUILD_NAME
ARG BUILD_REF
ARG BUILD_REPOSITORY
ARG BUILD_VERSION

# Labels
LABEL \
    io.hass.name="${BUILD_NAME}" \
    io.hass.description="${BUILD_DESCRIPTION}" \
    io.hass.arch="${BUILD_ARCH}" \
    io.hass.type="addon" \
    io.hass.version=${BUILD_VERSION} \
    maintainer="Frosh" \
    org.opencontainers.image.title="${BUILD_NAME}" \
    org.opencontainers.image.description="${BUILD_DESCRIPTION}" \
    org.opencontainers.image.vendor="Frosh Home Assistant Add-ons" \
    org.opencontainers.image.authors="Frosh" \
    org.opencontainers.image.licenses="MIT" \
    org.opencontainers.image.url="https://github.com/casse-boubou/hassio-addons" \
    org.opencontainers.image.source="https://github.com/${BUILD_REPOSITORY}" \
    org.opencontainers.image.documentation="https://github.com/${BUILD_REPOSITORY}/blob/main/README.md" \
    org.opencontainers.image.created=${BUILD_DATE} \
    org.opencontainers.image.revision=${BUILD_REF} \
    org.opencontainers.image.version=${BUILD_VERSION}
