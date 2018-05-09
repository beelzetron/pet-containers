# pet-fedora

[![Docker Repository on Quay](https://quay.io/repository/beelzetron/pet-containers/status "Docker Repository on Quay")](https://quay.io/repository/beelzetron/pet-containers)

This is my Fedora pet container image.
It includes some tools i use regularly in my sysadmin work.

To create the image i use [buildah](https://github.com/projectatomic/buildah):

`# cd pet-fedora && buildah bud -t pet-fedora:latest .`

I use [podman](https://github.com/projectatomic/libpod) to run it:

`# podman run -it --privileged --rm --dns 193.43.192.92 -v /home/lorenzodalrio:/home/lorenzodalrio docker.io/library/pet-fedora`

