FROM base/archlinux
MAINTAINER Magnus Therning <magnus@therning.org>

COPY pacman.conf /etc

RUN   true \
    && mkdir /repo \
    && touch /repo/repo.db \
    && pacman -Sy --noconfirm \
          base-devel \
          sudo \
    && true

RUN   true \
    && useradd -m -g users -G wheel -s /bin/bash hfa \
    && true

COPY sudoers /etc

USER hfa
