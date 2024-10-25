# ARRANCAR UN CONTENEDOR
### 1.
Iniciamos el contenedor de ubuntu con este comando:
`docker run -it --name ubuntu ubuntu:18.04`

Esto abrirá una sesión interactiva, saldremos de ella con el comando `exit`.

![img]()

### 2.
Después de salir verificamos el estado de los contenedores con el siguiente comando:
`docker ps -a`

![img]()

### 3.
Para reiniciar el siguiente comando:
`docker start ubuntu`

![img]()

### 4.
Una vez reiniciado, podemos verificar el contenedor con este estado:
`docker ps`

![img]()

### 5.
Para mostrar el contenido del archivo sin entrar al contenedor:
`docker exec ubuntu cat /etc/os-release`

![img]()

Este comando ejecuta cat /etc/os-release dentro del contenedor "ubuntu" y muestra el contenido en la terminal.