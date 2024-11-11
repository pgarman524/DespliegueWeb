# VOLÚMENES

## 1.
Primero, necesitamos crear los volúmenes `volumen_datos` y `volumen_web` usando el siguiente comando:

`sudo docker volume create volumen_datos | sudo docker volume create volumen_web`

![img]()


## 2.
Montamos el contenedor c1 con:

`docker run -d --name c1 -v volumen_web:/var/www/html php:7.4-apache`

y el contenedor c2 con:

`docker run -d --name c2 -v volumen_datos:/var/lib/mysql -e MYSQL_ROOT_PASSWORD=admin mariadb`

![img]()


## 3.
Con esto ya podemos parar sus procesos

`sudo docker stop c2`

Eliminamos  el contenedor c2:

`sudo docker rm c2`

Destruimos el volumen `volumen_datos` :

`sudo docker volume rm volumen_datos`

![img]()