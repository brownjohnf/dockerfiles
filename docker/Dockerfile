FROM brownjohnf/verto:verto as verto

FROM brownjohnf/alpine:master as main

CMD ["/bin/bash"]

RUN apk add --no-cache \
    docker

COPY --from=verto /usr/local/bin/verto /usr/local/bin/verto

