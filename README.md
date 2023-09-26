**Descarga la imagen 'httpd' y comprueba que está en tu equipo.**

*Comando para descargar httpd:*

    docker pull httpd

*Comando para comprobar si está en el qeuipo*:

    docker images

**Crea un contenedor con el nombre 'asir_httpd',mapea el puerto 80 del contenedor con el puerto 8000 de tu máquina y utiliza bind mount para que el directorio del apache2 'htdocs' este montado un directorio que tu elijas. **

    docker run -dit --name asir_httpd -p 8000:80 -v /home/asir2/SRI/Tarea2/cajones:/usr/local/apache2/htdocs httpd:2.4

**Realiza un 'hola mundo' en html y comprueba que accedes desde el navegador.**

*Creamos un html en el que escribimos "Hola mundo" y accedemos a el poniendo en el navegador:*

    localhost:8000/

**Crea un contenedor 'asir_web1' que use este mismo directorio para 'htdocs' y el puerto 8000**

*Comando para crear el contenedor y asignación de puerto*:

    docker run -dit --name asir_web1 -p 8000:80 -v /home/asir2/SRI/Tarea2/cajones:/usr/local/apache2/htdocs httpd:2.4

**Utiliza Code para hacer un hola mundo en html**

*Creamos un html con el texto "Hola mundo" y accedemos a el poniendo en el navegador:

    localhost:8000/

**Crea otro contenedor 'asir_web2' con el mismo directorio y a otro puerto, por ejemplo 9080.**

*Comando para crear el contenedor y asignación de puerto*:

    docker run -dit --name asir_web2 -p 9080:80 -v /home/asir2/SRI/Tarea2/cajones:/usr/local/apache2/htdocs httpd:2.4

    

