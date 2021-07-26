***Clase 4***

----
En esta clase hicimos una pequeña recapitulación.

***Un contenedor:*** Es un recipiente q corre en nuestra aplicacion tiene estados y es volatil, para  que la informacion persista se debe declarar un volumen dento de nuestro host.

***Las imagenes:*** No se pueden modificar, se creo a traves del dockerfile

***DOCKER COMPOSE***

**docker-alpine:** Es una imagen.
**nginx:**es una imagen tiene dos opciones, tiene varias capas

----


***Creando fichero compose
comandos utilizados***
 
Creamos la carpeta para el proyecto

***mkdir proxy***

luego,creamos y editamos el archivo Compose

***vim docker-compose.yml***

Utilizar los siguientes comandos:

***docker-compose up -d***

luego el comand

***docker-compose ps***

y en nuestro navegar vamos a nuestra direccion ip en el puerto 80 y podemos ver 
nuestro hostname: **abfde66b6e36**

para ver nuestros logs utlizamos el comando

***docker logs -f  proxy_web_1***

___________________________

***ESCALAMIENTO HORIZONTAL EN DOCKER COMPOSE***

Aprovecha todos los recursos 

***docker-compose down***

***docker-compose up --scale web=5 -d***

para tener redundancia en mis servicios


---------------------------
Clonamos el git 

***git clone https://github.com/jsgiraldoh/Jenkins.git***



***docker-compose -f docker-compose-jenkins.yml up -d***

**sudo chown manuel:manuel jenkins_home/**

***docker logs -f jenkins***

obtenemos la clave

y nos vamos a la direccion e ingresamos esta clave

***b6b33a388c9849ff8af86dffc0d33704***

Alli instalamos las herramientas necesarias de Jenkins.


