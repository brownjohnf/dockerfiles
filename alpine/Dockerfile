FROM library/alpine:latest as main

CMD ["/bin/bash"]

RUN apk add --no-cache \
    bash \
    curl \
    git \
    neovim \
    openssh \
  && ln -s $(which nvim) /usr/local/bin/vim

