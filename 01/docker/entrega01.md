# Instalación de Docker

## Desinstalación de docker desfasada:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/01_desinstalacion_versiones_anteriores.PNG)

Primero de todo vamos a desinstalar todo lo referente a docker por si acaso:
    `for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done`.

Con esto podemos empezar a instalar la nueva versión.


## Instalación de docker:

Primero de todo debemos añadir el repositorio de docker con `apt`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/02_instalacion_docker_part01.PNG)

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/02_instalacion_docker_part02.PNG)

Dejo aquí los comandos utilizados:
`sudo apt-get update
sudo apt-get install ca-certificates curl
sudo install -m 0755 -d /etc/apt/keyrings
sudo curl -fsSL https://download.docker.com/linux/debian/gpg -o /etc/apt/keyrings/docker.asc
sudo chmod a+r /etc/apt/keyrings/docker.asc`.

Después añadimos el repositorio a `apt`:
`echo \
  "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/debian \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \
  sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/02_instalacion_docker_part03.PNG)


## Instalación de paquetes de Docker

Para instalar la última versión:
`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`

Verificamos la instalación:
`sudo docker run hello-world`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/03_hello_world_docker.PNG)

Este comando descarga una imagen test del contenedor. Cuando este lo encuentra, nos imprime el mensaje de confirmación.
