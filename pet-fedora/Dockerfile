FROM registry.fedoraproject.org/fedora:28

MAINTAINER Lorenzo Dalrio <lorenzo.dalrio@gmail.com>

RUN dnf -y install sudo mock rpmdevtools rpm-build rpmlint git bash-completion \
    && dnf clean all

RUN groupadd -g 1000 lorenzodalrio \
    && useradd -g lorenzodalrio -G wheel,mock -u 1000 -m lorenzodalrio

RUN echo "%wheel ALL=(ALL) NOPASSWD: ALL" >> /etc/sudoers.d/wheel

RUN echo "config_opts['use_nspawn'] = False" >> /etc/mock/site-defaults.cfg

RUN dnf -y install java-1.8.0-openjdk-devel \
                   patch \
                   unzip \
                   wget \
                   xmlstarlet \
                   tmux \
                   powerline \
                   powerline-fonts \
                   vim-powerline \
                   tmux-powerline \
                   vim-enhanced \
                   tmux \
                   powerline \
                   powerline-fonts \
                   vim-powerline \
                   tmux-powerline \
                   vim-enhanced \
                   ansible \
                   ansible-lint \
                   python2-requests \
                   less \
                   man-pages \
                   man-db \
                   iputils \
                   openldap-clients \
                   buildah \
    && dnf clean all

VOLUME /home/lorenzodalrio

WORKDIR /home/lorenzodalrio

ENV LANG en_US.UTF-8

USER lorenzodalrio
CMD ["/bin/bash"]

