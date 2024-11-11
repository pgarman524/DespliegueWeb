# GESTIÓN DE IMÁGENES

## 1.
Descargamos la imagen de Ubuntu:

`sudo docker pull ubuntu:20.04`

![img]()


## 2.
Obtenemos toda la información de la imagen descargada, usamos el comando `docker inspect` seguido del nombre de la imagen:

`sudo docker inspect ubuntu:20.04 > info.txt`

![img]()


## 3.
Para crear un contenedor a partir de la imagen **ubuntu:20.04** y nombrarlo **modulo3**, usamos el siguiente comando:

`sudo docker run -d --name modulo3 ubuntu:20.04`

![img]()


## 4.
Verificamos que el contenedor ha sido creado y si está en ejecución:

`sudo  docker ps -a`

![img]()


## 5.
Para borrar el archivo usaríamos este comando:

`sudo docker rmi ubuntu:20.04`

![img]()

Pero no nos dejará hacerlo ya que aún no hemos parado la imagen, aunque podemos hacerlo con un parámetro `-f` para forzar la acción.

## 6.
Vamos a hacer los pasos necesarios para borrar la imagen sin usar `-f`. Con estos comandos:

`sudo docker stop modulo3`
`sudo docker rm modulo3`
`sudo docker rmi ubuntu:20.04`

![img]()


Y con esto habríamos borrado la imagen de ubuntu.
