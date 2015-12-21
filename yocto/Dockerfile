FROM ubuntu:14.04

RUN apt-get update && \
    apt-get install -y gawk wget git-core diffstat unzip texinfo \
    gcc-multilib build-essential chrpath socat libsdl1.2-dev xterm \
    python-ply python-progressbar python-bs4 python-pyinotify

# Install bitbake
ENV HOME /root
WORKDIR $HOME
RUN git clone git://git.openembedded.org/bitbake.git --branch 1.26.0 bitbake
WORKDIR bitbake
RUN python ./setup.py install
WORKDIR $HOME
RUN rm -rf bitbake
