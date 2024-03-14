FROM ubuntu:latest

# Evita preguntas al instalar paquetes
ARG DEBIAN_FRONTEND=noninteractive

# Actualiza e instala dependencias necesarias
RUN apt-get update && apt-get install -y \
    software-properties-common \
    && add-apt-repository ppa:alexis.bienvenue/amc \
    && apt-get update \
    && apt-get install -y auto-multiple-choice

# Configura el entorno de ejecución
CMD ["/usr/bin/auto-multiple-choice"]
