# **Sesión 1 - Imágenes - Ejercicios para entregar**


### Servidor web

- Arranca un contenedor que ejecute una instancia de la imagen `php:7.4-apache`, que se llame `web` y que sea accesible desde tu equipo en el puerto 8000.
  
  ![img1](img/img1.PNG)

- Colocar en el directorio raíz del servicio web (`/var/www/html`) de dicho contenedor un fichero llamado `index.html` con el siguiente contenido:

        `<h1>HOLA SOY XXXXXXXXXXXXXXX</h1>`

Deberás sustituir XXXXXXXXXXX por tu nombre y tus apellidos.

- Colocar en ese mismo directorio raíz un archivo llamado `index.php` con el siguiente contenido:

        `<?php echo phpinfo(); ?>`

- Para crear los ficheros tienes tres alternativas:
    - Ejecutando bash de forma interactiva en el contenedor y creando los ficheros.
    

    - Ejecutando un comando `echo` en el contenedor con `docker exec`.
    
    - Usando docker cp como hemos visto en el ejercicio 5.


    ![img2](img/img2.PNG)
  
    ![img3](img/img3.PNG)
  
    ![img4](img/img4.PNG)

### Servidor de base de datos

- Arrancar un contenedor que se llame bbdd y que ejecute una instancia de la imagen mariadb para que sea accesible desde el puerto 3336.

- Antes de arrancarlo visitar la página del contenedor en Docker Hub y establecer las variables de entorno necesarias para que:
    - La contraseña de root sea root.
    - Crear una base de datos automáticamente al arrancar que se llame prueba.
    - Crear el usuario invitado con las contraseña invitado.

![img5](img/img5.PNG)

Deberás entregar los siguientes pantallazos comprimidos en un zip o en un documento pdf:

- Pantallazo que desde el navegador muestre el fichero index.html.

![img6](img/img6.PNG)

- Pantallazo que desde el navegador muestre el fichero index.php.

![img7](img/img7.PNG)

- Pantallazo donde se vea el tamaño del contenedor web después de crear los dos ficheros.

![img8](img/img8.PNG)

- Pantallazo donde desde un cliente de base de datos (instalado en tu ordenador) se pueda observar que hemos podido conectarnos al servidor de base de datos con el usuario creado y que se ha creado la base de datos prueba (show databases). El acceso se debe realizar desde el ordenador que tenéis instalado docker, no hay que acceder desde dentro del contenedor, es decir, no usar docker exec.

He utilizado el programa dbeaver

![img4](img/img9.PNG)
![img10](img/img10.PNG)

- Pantallazo donde se comprueba que no se puede borrar la imagen mariadb mientras el contenedor bbdd está creado.

![img11](img/img11.PNG)
