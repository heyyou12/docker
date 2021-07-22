## Clase 2

Para la segunda clase empezamos con la configuracion de los equipos
e instalacion de las herramientas a utilizar.

1. Utilizamos la maquina virtual Ubuntu

2. Para la correcta configuracion de docker y escritura de los comandos utilizamos una herramienta llamada ***MobaXterm***

Alli utilizamos el comando **sudo apt-get update** para actualizar, luego utilizamos el comando **ap a s** para conocer la ip para el siguiente paso.

Seguido utilizamos la siguiente instruccion **ssh 192.168.0.22 -l manuel**, luego se instalaron los paquetes para permitir el uso de un repositorio sobre HTTPS, con la siguiente instruccion: 

***sudo apt-get install \
apt-transport-https \
ca-certificates \
curl \
gnupg-agent \
software-properties-common***

3. Agregamos la clave GPG oficial de Docker

***curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -***

4. Con el siguiente comando configuramos el repositorio estable

***echo \
  "deb [arch=amd64 signed-by=/usr/share/keyrings/docker-archive-keyring.gpg] https://download.docker.com/linux/ubuntu \
  $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null***

5. Se instala la version para comunidad, Docker CE

***sudo apt-get install docker-ce docker-ce-cli containerd.io***

6. Se agrego el usuario de Docker

***sudo usermod -aG docker ubuntu***

7. El primer contenedor

***sudo docker run hello-world***

8. Se comprueba la version

***sudo docker version***

## Instalacion Docker Compose

1. Utilizamos el siguiente comando para descargar la version estable

***sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose***

2. le aplicamos los permisos ejecutables con la instruccion

***sudo chmod +x /usr/local/bin/docker-compose***

3. Nos posicionamos sobre la carpeta ***Codimd***

4. Luege ejecutamos la siguiente instruccion ***sudo docker-compose up -d***





