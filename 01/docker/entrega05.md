# OBTENIENDO INFORMACIÓN DE CONTENEDORES

### 1.
Para obtener la dirección IP del contenedor baseDatos:

`docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' baseDatos`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act05/01_direccion_IP_contenedor.PNG)

### 2.
Para obtener la redirección de puertos del contenedor baseDatos:

`docker port baseDatos`

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act05/02_redireccion_puertos.PNG)

### 3.
Realizamos las mismas acciones para web2:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/docker/imagenes/act05/03_repetición.PNG)
