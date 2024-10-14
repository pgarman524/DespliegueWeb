# Intalación DNS
## 1. Instalar paquetes.
Instalamos los paquetes `bind9`, `bind9utils` y `bind9-doc`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/01_Instalacion_Bind9.PNG)  
![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/02_Instalacion_Bind9.PNG)    

Tras ello instalamos `net-tools`.

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/03_Instalacion_Bind9.PNG)  

## 2. Modificar configuración DNS
Usamos un editor de md como es el `nano` y usamos el comando:  
    `sudo nano /etc/bind/named.conf.options`  
Para así editar el texto de su interior

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/05_ConfigurarDNS.PNG)  

Descomentamos el texto y lo modificamos con el puerto `8.8.8.8`. 

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/06_ConfigurarDNS.PNG)

Añadimos también este puerto extra:  

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/07_ConfigurarDNS.PNG)

A continuación escribimos el comando:  
`sudo nano /etc/bind/db.example.com`  
Esto nos ayudará a crear el archivo de configuración qeu está en un principio vacío, por lo que deberemos rellenarlo con este texto:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/09_ConfigurarDNS.PNG)

Esta sería la configuración de nuestro DNS.

También deberemos crear otro archivo con estos datos en su interior usando `sudo nano`.  

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/11_ConfigurarDNS.PNG)

Para finalizar otro archivo con este texto:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/12_ConfigurarDNS.PNG)

Y con ello ya podríamos comprobar que todo funciona correctamente utilizando el comando `sudo systemctl status bind9`:

![img](https://github.com/pgarman524/DespliegueWeb/blob/master/01/DNS/capturas/13_ConfigurarDNS.PNG).

