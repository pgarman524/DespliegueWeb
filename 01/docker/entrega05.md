# OBTENIENDO INFORMACIÓN DE CONTENEDORES

### 1.
Para obtener la dirección IP del contenedor baseDatos:

`docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' baseDatos`

![img]()

### 2.
Para obtener la redirección de puertos del contenedor baseDatos:

`docker port baseDatos`

![img]()

### 3.
Realizamos las mismas acciones para web2:

![img]()