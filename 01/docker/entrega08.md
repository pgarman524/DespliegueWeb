# BIND MOUNTS

## 1.
Primero de todo crearemos la carpeta con el comando `mkdir`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act08/01_crear_carpeta.PNG)

Creamos el archivo *index.html* dentro de la carpeta saludo usando este comando:

`echo "<h1>HOLA SOY Pablo García Mangana</h1>" > saludo/index.html`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act08/02_crear_index.html_texto.PNG)

Verificamos que ha sido creado correctamente con `cat`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act08/02_verificamos_texto.PNG)

## 2.
Ahora vamosa  crear y arrancar los dos contenedores php y que hagan un **bind mount** de la carpeta *saludo* en un html.

Para eso usamos el comando:

`docker run -d --name c2 -p 8181:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act08/03_creamos_phpContainer.PNG)

y para el siguiente usamos:

`docker run -d --name c2 -p 8282:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act08/03_creamos_phpContainerC3.PNG)

## 3.
Verificamos con `docker ps` que funcionan correctamente:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act08/03_verificamos_contenedores_PHP.PNG)

Como vemos, funcionan correctamente.

## 4.
Ahora para ver desde la terminal que funciona correctamente he usado el comando `curl`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act08/04_URL_mostrar_bash.PNG)

Ya estarían los html correctamente funcionando em el servidor local.
