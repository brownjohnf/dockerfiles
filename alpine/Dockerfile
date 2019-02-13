FROM library/alpine:latest as main

CMD ["/bin/bash"]

RUN apk add --no-cache \
    bash \
    git \
    neovim \
    openssh \
  && ln -s $(which nvim) /usr/local/bin/vim

