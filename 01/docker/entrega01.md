## Desinstalación de docker desfasada:

![img](imagen)

Primero de todo vamos a desinstalar todo lo referente a docker por si acaso:
    `for pkg in docker.io docker-doc docker-compose podman-docker containerd runc; do sudo apt-get remove $pkg; done`.

Con esto podemos empezar a instalar la nueva versión.

## Instalación de docker:

Primero de todo debemos añadir el repositorio de docker con `apt`.

![img](imagen)

![img](imagen)

![img](imagen)

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

![img](imagen)


## Instalación de paquetes de Docker

![img](imagen)

Para instalar la última versión:
`sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin`

![img](imagen)

Verificamos la instalación:
`sudo docker run hello-world`

![img](imagen)

Este comando descarga una imagen test del contenedor. Cuando este lo encuentra, nos imprime el mensaje de confirmación.