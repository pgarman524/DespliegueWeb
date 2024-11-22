# DOCKERFILE

## 1a Parte

### 1.
Creamos el contenedor de `ubuntu: 20.40` con el comando:

`docker run -it ubuntu:20.04 bash`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/01_montar_Ubuntu.PNG)

### 2.
Instalamos todos los programas requeridos, para ello primero actualizamos las apt.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/01_montar_Ubuntu.PNG)

Luego empezamos a instalar: *nano*, *vim*, *inetutils-tools*, *dnsutils*

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/03_instalar_programas.PNG)

Solo pondré el ejemplo con nano.


### 3.
Creamos el usuario *usuario*  con contraseña *usuario*:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/04_crear_user_user.PNG)

### 4.
Tras acabar de instalar todos los paquetes usamos `exit` para volver a nuestra consola de linux y procedemos a guardar el contenedor en una nueva imagen, pero primero necesitamos la **ID** de la imagen de ubuntu. Por ello utilizamos este comando: 

`docker ps -a`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/05_docker_ID.PNG)

Visto ya la **ID**, podemos pasar a guardar el estado de la imagen:

`docker commit 2e2b0b0bc030 garmanpaDockerHub/a61`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/06_guardar_imagen.PNG)

Nos logueamos en docker.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/07_iniciarsesion_docker.PNG)

Y finalmente ya podemos subir la imagen creada:
`docker push garmanpaDockerHub/a61`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/08_upload_imagen_creada.PNG)


## 2a Parte

### 1.
Abrimos un nano para colocar las instrucciones del php:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/10_Part02_crearDockerfile.PNG)

### 2.
Lanzamos la imagen de php:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/11_Part02_push_docker.PNG)

### 3.
Subimos la imagen a nuestro servidor:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act10/12_Part02_docker%20push.PNG)

Finalmente, ya tendríamos subido nuestro docker.


## 2a Parte
