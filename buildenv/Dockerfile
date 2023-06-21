FROM randomdude/gcc-cross-x86_64-elf

RUN sed -i 's/stretch/buster/g' /etc/apt/sources.list

RUN apt-get update
RUN apt-get upgrade -y --allow-unauthenticated
RUN apt-get install -y nasm --allow-unauthenticated
RUN apt-get install -y xorriso --allow-unauthenticated
RUN apt-get install -y grub-pc-bin --allow-unauthenticated
RUN apt-get install -y grub-common --allow-unauthenticated

VOLUME /root/env
WORKDIR /root/env
