Clase 3
===
1. Creamos una carpeta utilizando el comando
***mkdir mi-primer-dockerfile***

nos paramos en el directorio
***cd mi-primer-dockerfile***

alli creamos el Dockerfile utilizando el comando
***vim Dockerfile***
oprimimos la tecla i y copiamos 

***FROM nginx
COPY static-html-directory /usr/share/nginx/html***

salimos del editor vim con ***:wq***

creamos el directorio utilizando el comando
***mkdir static-html-directory***

nos vamos al directorio 
***cd static-html-directory***

utlizamos nuestro editor de texto vim
***vim index.html***

y copiamos algun texto
**"prueba curso semillero"**

salimos al expacio de trabajo donde esta nuestro dockerfile

luego vamos a construir nuestro comando de construccion 
utilizando el comando
***docker image build -t some-content-nginx .***

alli vamos a correr nuestro primer contenedor con el siguiente comando
***docker run --name some-nginx -d -p 8080:80 some-content-nginx***

ahora utilizamos el comando
***curl -k localhost:8080***

Podemos ver el mensaje que habiamos creado, luego en nuestro navegador utilizando nuestra ip podemos ver que efectivamente
ya esta corriendo nuestro sitio web. 


------------------------

2. Tenemos la opcion de guardar el estado del contenedor utilizando el comando 
***docker commit 174f7da5405a nginx-final***

luego detenemos nuestro contenedor
***docker stop some-nginx***

confirmamos con el comando
***docker ps -a***

ahora con nuestra imagen vamos correr nuestro servidor
***docker run --name nginx-final -d -p 8080:80 nginx-final***

y vemos nuestro contenedor corriendo con la imagen creada a partir del contenedor corriendo
______________________

3. Creamos un usuario en dockerhub
nos logueamos a la pagina por medio de la consola de comandos 
utilizando el comando

***docker login***

luego utilizamos el comando 

***docker tag some-content-nginx heyyou12/fedesoft-web***

luego debemos hacer push al repo utilizando el comando
***docker push heyyou12/fedesoft-web***

y ya se puede ver en la pagina

para descargar utilizamos en comando
***docker pull heyyou12/fedesof-web***

y lo ejecutamos con el comando 
***docker run --name fedesof-web -d -p 8081:80 heyyou12/fedesof-web***