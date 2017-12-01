# Cofiguración de Ansible

**Se instalaran  y configuraran estos 2 servicios:**

* Apache
* Munin

## Primer paso, instalación del servidor web

**instalamos el servidor web en el name_web_server**

## Instalacion de Apache

**utilizamos el sguiente comando en nuestra terminal:**

`ansible-playbook -i hosts install_apache.yml`

![alt-text](/Images/1.png)

## Instalacion de Munin

Intalamos Munin en el name_web_server

**utilizamos el sguiente comando en nuestra terminal:**

`ansible-playbook -i hosts install_munin.yml`

![alt-text](/Images/2.png)

## Iniciar el servicio de Apache

**Desde el servidor iniciamos los servicios de Apache 2:**

`service apache2 start`

Despues ingresamos nuevamente por medio del navegador web a la ruta `127.0.0.1`

![alt-text](/Images/3.png)

Ahora dese otra pestaña ingresamos al index de munin previamente configurado

![Munin](/Images/4.png)

como vemos en la imagen anterior se nos presento un error con el munin
