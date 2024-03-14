# Nombre de la imagen Docker
IMAGE_NAME=amc-ubuntu

# IP del host para la visualización X11 (modifica con tu IP o usa una variable de entorno)
HOST_IP ?= $(ipconfig getifaddr en0)
# Puerto para la visualización X11 (el predeterminado es 0, pero puede cambiar según tu configuración)
DISPLAY_PORT ?= 0


# Carpeta local que deseas compartir con el contenedor
LOCAL_QUIZZES_FOLDER=./quizzes
# Ruta en el contenedor donde se montará la carpeta compartida
CONTAINER_QUIZZES_FOLDER=/home/amc/quizzes

# Construye la imagen Docker
build:
	docker build -t $(IMAGE_NAME) .

# Ejecuta la imagen Docker
run:
	# xhost + ${HOST_IP}
	docker run -it --entrypoint /bin/bash  -v $(LOCAL_QUIZZES_FOLDER):$(CONTAINER_QUIZZES_FOLDER) $(IMAGE_NAME) 

.PHONY: build run
