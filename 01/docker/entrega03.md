# ARRANCAR UN CONTENEDOR
### 1.
Iniciamos el contenedor de ubuntu con este comando:
`docker run -it --name ubuntu ubuntu:18.04`

Esto abrirá una sesión interactiva, saldremos de ella con el comando `exit`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act03/01.PNG)

### 2.
Después de salir verificamos el estado de los contenedores con el siguiente comando:
`docker ps -a`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act03/02.PNG)

### 3.
Para reiniciar el siguiente comando:
`docker start ubuntu`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act03/03.PNG)

### 4.
Una vez reiniciado, podemos verificar el contenedor con este estado:
`docker ps`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act03/04.PNG)

### 5.
Para mostrar el contenido del archivo sin entrar al contenedor:
`docker exec ubuntu cat /etc/os-release`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act03/05.PNG)

Este comando ejecuta cat /etc/os-release dentro del contenedor "ubuntu" y muestra el contenido en la terminal.
