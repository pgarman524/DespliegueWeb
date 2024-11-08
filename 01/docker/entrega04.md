# EJECUCIÓN DE SERVICIOS DESDE CONTENEDORES
### 1.
Primero, vamos a arrancar un contenedor que ejecute un servidor web Apache con PHP 7.3. Este contenedor estará disponible en el puerto 8181. 

`docker run -d --name web -p 8181:80 php:7.3-apache`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act04/01_php.PNG)

### 2.
Una vez el contenedor esté ejecutándose, vamos a crear el archivo index.html con el contenido adecuado. Dentro de este index escribiremos:

`<h1>HOLA SOY Pablo García Mangana</h1>`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act04/01_php.PNG)

### 3.
Luego, copiamos el archivo index.html al directorio raíz del servidor web dentro del contenedor. 

`docker cp index.html web2:/var/www/html/index.html`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act04/03_copiadodelIndex.PNG)

### 4.
De igual forma, creamos un archivo llamado index.php en tu máquina local y agrega el siguiente contenido. 

`<?php phpinfo(); ?>`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act04/03_copiadodelIndex.PNG)

### 5.
Luego, copiamos este archivo al directorio raíz del servidor web en el contenedor con: 

`docker cp index.php web:/var/www/html/index.php`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act04/05_copiadodelIndexPHP.PNG)

### 6.
Ahora, vamos a arrancar el contenedor de MariaDB con la configuración solicitada. 

`docker run -d --name baseDatos -p 3336:3306 \
  -e MYSQL_ROOT_PASSWORD=root \
  -e MYSQL_DATABASE=prueba \
  -e MYSQL_USER=invitado \
  -e MYSQL_PASSWORD=invitado \
  mariadb
`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act04/06_Crear_contenedor_Mariadb.PNG)

### 7.
Podemos verificar que el contenedor de MariaDB está funcionando correctamente ejecutando: 

`docker logs bbdd`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act04/07_Comprobar_Mariadb.PNG)
