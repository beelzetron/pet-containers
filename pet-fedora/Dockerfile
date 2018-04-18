FROM registry.fedoraproject.org/fedora:27

MAINTAINER Lorenzo Dalrio <lorenzo.dalrio@gmail.com>

RUN dnf -y install sudo git tmux powerline powerline-fonts \
    vim-powerline tmux-powerline nmap mock rpm-build rpmlint \
    vim-enhanced ansible ansible-lint bash-completion \
    python2-requests less man-pages man-db iputils \
    && dnf clean all

RUN groupadd -g 1000 lorenzodalrio \
    && useradd -g lorenzodalrio -G wheel,mock -u 1000 -m lorenzodalrio

RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers.d/wheel

VOLUME /home/lorenzodalrio

WORKDIR /home/lorenzodalrio

ENV LANG en_US.UTF-8

USER lorenzodalrio
CMD ["/bin/bash"]

