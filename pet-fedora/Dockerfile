FROM registry.fedoraproject.org/fedora:28

MAINTAINER Lorenzo Dalrio <lorenzo.dalrio@gmail.com>

RUN groupadd -g 1000 lorenzodalrio \
    && useradd -g lorenzodalrio -G wheel -u 1000 -m lorenzodalrio

RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers.d/wheel

RUN dnf -y install sudo git tmux powerline powerline-fonts \
    vim-powerline tmux-powerline nmap rpm-build rpmlint \
    vim-enhanced ansible ansible-lint bash-completion \
    python2-requests less man-pages man-db iputils openldap-clients \
    && dnf clean all

VOLUME /home/lorenzodalrio

WORKDIR /home/lorenzodalrio

ENV LANG en_US.UTF-8

USER lorenzodalrio
CMD ["/bin/bash"]

