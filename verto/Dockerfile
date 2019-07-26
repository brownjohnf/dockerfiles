FROM library/rust:latest as verto
WORKDIR /src

ENV VERTO_VERSION 0.0.3
RUN apt-get update && apt-get install -y curl
RUN curl --silent \
    https://gitlab.com/jack/verto/-/archive/${VERTO_VERSION}/verto-${VERTO_VERSION}.tar.gz \
  | tar -xz -C /src --strip-components 1
RUN cargo build --release

FROM scratch as main

ENTRYPOINT ["/verto"]

COPY --from=verto /src/target/release/verto /usr/local/bin/verto

