# Configuraciones y creación de dockers de prueba

Para esta configuracion se tendran en cuenta varios pasos para la realizacion que son los siguientes

## Primer paso
Se debe construir un docker personalizado que incluye el servidor openssh

-Con el Dockerfile construiremos la imagen de nuestros dockers. 

Usaremos el siguiente comando en nuestra consola: 
               
               docker build -t server:16.04 .

![alt-text](/imagenes/creacion)

![alt-text](/imagenes/verificacion)

## Segundo paso, despliege

Ahora debes crear una maquinas para el despliegue, se creará  un servidor Apache.

Usamos el siguiente comando en nuestra consola: 

docker run -d -P --name danilo_web_server -p 2221:22 -p 80:80 server:16.04

![alt-text](/imagenes/parte3)

despues le damos permisos a la llave con el comando:

				chmod 0600 key.private

# tercer paso,Adicionar las llaves ssh</h3>

Usamos los siguientes comandos en nuestra consola: 

ssh -o StrictHostKeyChecking=no root@127.0.0.1 -p 2221 -i key.private hostname

