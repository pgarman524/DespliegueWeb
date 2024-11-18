# DOCKERFILE

## 1a Parte

### 1.
Creamos el contenedor de `ubuntu: 20.40` con el comando:

`docker run -it ubuntu:20.04 bash`

![img]()

### 2.
Instalamos todos los programas requeridos, para ello primero actualizamos las apt.

![img]()

Luego empezamos a instalar: *nano*, *vim*, *inetutils-tools*, *dnsutils*

![img]()

Solo pondré el ejemplo con nano.


### 3.
Creamos el usuario *usuario*  con contraseña *usuario*:

![img]()

### 4.
Tras acabar de instalar todos los paquetes usamos `exit` para volver a nuestra consola de linux y procedemos a guardar el contenedor en una nueva imagen, pero primero necesitamos la **ID** de la imagen de ubuntu. Por ello utilizamos este comando: 

`docker ps -a`

![img]()

Visto ya la **ID**, podemos pasar a guardar el estado de la imagen:

`docker commit 2e2b0b0bc030 garmanpaDockerHub/a61`

![img]()

Nos logueamos en docker.

![img]()

Y finalmente ya podemos subir la imagen creada:
`docker push garmanpaDockerHub/a61`

![img]()


## 2a Parte