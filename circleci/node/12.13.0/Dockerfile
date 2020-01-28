FROM circleci/node:12.13.0

RUN sudo apt-get install awscli

RUN curl -fsSL https://raw.githubusercontent.com/Linuxbrew/install/master/install.sh | bash

ENV HOMEBREW_PREFIX=/home/linuxbrew/.linuxbrew
ENV HOMEBREW_CELLAR=/home/linuxbrew/.linuxbrew/Cellar
ENV HOMEBREW_REPOSITORY=/home/linuxbrew/.linuxbrew/Homebrew
ENV PATH=/home/linuxbrew/.linuxbrew/bin:/home/linuxbrew/.linuxbrew/sbin:$PATH
ENV MANPATH=/home/linuxbrew/.linuxbrew/share/man:${MANPATH}
ENV INFOPATH=/home/linuxbrew/.linuxbrew/share/info:${INFOPATH}

RUN brew update

RUN brew tap aws/tap
RUN brew install aws-sam-cli
