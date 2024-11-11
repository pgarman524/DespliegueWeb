# GESTIÓN DE IMÁGENES

## 1.
Descargamos la imagen de Ubuntu:

`sudo docker pull ubuntu:20.04`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act06/01_descargar_ubuntu.PNG)


## 2.
Obtenemos toda la información de la imagen descargada, usamos el comando `docker inspect` seguido del nombre de la imagen:

`sudo docker inspect ubuntu:20.04 > info.txt`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act06/02_obtener_txt_instanciar_imagen.PNG)


## 3.
Para crear un contenedor a partir de la imagen **ubuntu:20.04** y nombrarlo **modulo3**, usamos el siguiente comando:

`sudo docker run -d --name modulo3 ubuntu:20.04`


## 4.
Verificamos que el contenedor ha sido creado y si está en ejecución:

`sudo  docker ps -a`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act06/03_verificar_imagen.PNG)



## 5.
Para borrar el archivo usaríamos este comando:

`sudo docker rmi ubuntu:20.04`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act06/04_intento_borrado.PNG)

Pero no nos dejará hacerlo ya que aún no hemos parado la imagen, aunque podemos hacerlo con un parámetro `-f` para forzar la acción.

## 6.
Vamos a hacer los pasos necesarios para borrar la imagen sin usar `-f`. Con estos comandos:

`sudo docker stop modulo3`
`sudo docker rm modulo3`
`sudo docker rmi ubuntu:20.04`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act06/05_pasos_de_borrado.PNG)


Y con esto habríamos borrado la imagen de ubuntu.
