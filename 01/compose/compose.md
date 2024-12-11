# Instalación compose

## 1.
Instalamos docker para poder trabajar con él:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/compose/imagenes/01_instalar.PNG)

Luego instalamos Docker Compose utilizando los siguientes comandos:

`sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose`

`sudo chmod +x /usr/local/bin/docker-compose`

Luego lo verificaremos usando:
`docker-compose --version`ç

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/compose/imagenes/02_docker.PNG)

## 2.
Creamos un directorio para el proyecto y entonces añadimos al archivo **.yml** los datos necesarios usando un `nano`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/compose/imagenes/03_crear_mediawiki_docker.PNG)

## 3.
Una vez creado el archivo `docker-compose.yml`, levantamos los contenedores con el siguiente comando:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/compose/imagenes/04_levantar_compose.PNG)

## 4.
Tras esto podemos entrar en nuestra página web con un `http://localhost`. Este nos mostraría la página de instalación donde colocaríamos las opciones que necesitemos.
