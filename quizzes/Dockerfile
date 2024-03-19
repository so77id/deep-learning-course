FROM ubuntu:latest

# Evita preguntas al instalar paquetes
ARG DEBIAN_FRONTEND=noninteractive

# Actualiza e instala dependencias necesarias
RUN apt-get update
RUN apt-get install -y software-properties-common

RUN add-apt-repository ppa:alexis.bienvenue/amc 
RUN apt-get update 
RUN apt-get install -y auto-multiple-choice

RUN apt-get install -y evince
RUN apt-get install -y texmaker

# Configura el entorno de ejecución
CMD ["/usr/bin/auto-multiple-choice"]
