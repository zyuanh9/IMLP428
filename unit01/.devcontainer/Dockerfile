FROM quay.io/jupyter/minimal-notebook:ubuntu-24.04

USER root
RUN export HOME=/root

RUN apt-get update
RUN apt-get install -y vim net-tools iputils-ping dnsutils zsh less lsof make
RUN pip install ipykernel -U --user --force-reinstall

RUN git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.oh-my-zsh
RUN cp ~/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
RUN chsh -s $(which zsh)

# RUN pip install Django
# RUN pip install autopep8
# RUN pip install django-bootstrap-v5
# RUN pip install whitenoise

ENV MAINTAINER=zyuanh9@gmail.com

ENTRYPOINT [ "zsh" ]