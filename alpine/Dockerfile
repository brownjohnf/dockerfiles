FROM brownjohnf/verto:verto as verto

FROM library/alpine:latest as main

CMD ["/bin/bash"]

RUN apk add --no-cache \
    bash \
    curl \
    git \
    jq \
    neovim \
    openssh \
    wget \
  && ln -s $(which nvim) /usr/local/bin/vim

RUN wget -O /usr/local/bin/yq \
    https://github.com/mikefarah/yq/releases/download/2.2.1/yq_linux_amd64 \
  && chmod +x /usr/local/bin/yq

COPY --from=verto /usr/local/bin/verto /usr/local/bin/verto

