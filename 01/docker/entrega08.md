# BIND MOUNTS

## 1.
Primero de todo crearemos la carpeta con el comando `mkdir`.

![img]()

Creamos el archivo *index.html* dentro de la carpeta saludo usando este comando:

`echo "<h1>HOLA SOY Pablo García Mangana</h1>" > saludo/index.html`

![img]()

Verificamos que ha sido creado correctamente con `cat`.

![img]()

## 2.
Ahora vamosa  crear y arrancar los dos contenedores php y que hagan un **bind mount** de la carpeta *saludo* en un html.

Para eso usamos el comando:

`docker run -d --name c2 -p 8181:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache`

![img]()

y para el siguiente usamos:

`docker run -d --name c2 -p 8282:80 -v $(pwd)/saludo:/var/www/html php:7.4-apache`

![img]()

## 3.
Verificamos con `docker ps` que funcionan correctamente:

![img]()

Como vemos, funcionan correctamente.

## 4.
Ahora para ver desde la terminal que funciona correctamente he usado el comando `curl`.

![img]()

Ya estarían los html correctamente funcionando em el servidor local.
