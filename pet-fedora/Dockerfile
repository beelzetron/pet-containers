FROM registry.fedoraproject.org/fedora:28

MAINTAINER Lorenzo Dalrio <lorenzo.dalrio@gmail.com>

RUN groupadd -g 1000 lorenzodalrio \
    && useradd -g lorenzodalrio -G wheel -u 1000 -m lorenzodalrio

RUN dnf -y install sudo git tmux powerline powerline-fonts xmlstarlet \
    vim-powerline tmux-powerline nmap rpm-build rpmlint java-1.8.0-openjdk-devel \
    vim-enhanced ansible ansible-lint bash-completion patch unzip wget \
    python2-requests less man-pages man-db iputils openldap-clients \
    mock rpmdevtools \
    && dnf clean all

RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers.d/wheel

VOLUME /home/lorenzodalrio

WORKDIR /home/lorenzodalrio

ENV LANG en_US.UTF-8

USER lorenzodalrio
CMD ["/bin/bash"]

