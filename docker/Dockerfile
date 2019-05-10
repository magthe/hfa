FROM archlinux/base:latest
MAINTAINER Magnus Therning <magnus@therning.org>

COPY pacman.conf /etc

RUN   true \
    && mkdir /repo \
    && touch /repo/repo.db \
    && mkdir /mtrepo \
    && touch /mtrepo/mtrepo.db \
    && pacman -Sy --noconfirm --needed \
          base-devel \
          sudo \
          bind-tools \
    && rm /mtrepo/mtrepo.db \
    && true

RUN   true \
    && useradd -m -g users -G wheel -s /bin/bash hfa \
    && true

COPY sudoers /etc

USER hfa

VOLUME ["/mtrepo"]
