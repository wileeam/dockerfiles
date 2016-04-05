FROM phusion/baseimage:latest
MAINTAINER Guillermo Rodríguez Cano <gurc@csc.kth.se>

# Use baseimage-docker's init system.
CMD ["/sbin/my_init"]

#RUN apt-get update && apt-get install -y git texlive-full
RUN apt-get update --fix-missing -qq -y \
  && apt-get install -y \
    texlive-latex-base \
    texlive-xetex \ 
    latex-xcolor \ 
    latexmk \ 
    texlive-math-extra \
    texlive-latex-extra \
    texlive-fonts-extra \
    curl \
    wget \  
    git \
    fontconfig \ 
    make \ 
    uuid-runtime

# Clean up APT when done.
RUN apt-get clean && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
