# telematica
pasos para realizar la instalacion de la aplicacion 
primer paso la clonacion del repositorio 

HTTPS https://github.com/jsam2001/telematica.git

SSH   https://github.com/jsam2001/telematica.git

# Para tener encuenta 
Si estás ejecutando esta aplicación en la nube, es importante realizar algunos ajustes en el archivo web.py para asegurarte de que funcione correctamente. Uno de los cambios necesarios implica reemplazar la dirección "localhost" por tu dirección IP pública. La dirección IP pública es la que identifica tu dispositivo en Internet y permite que otros equipos accedan a tu aplicación.

Para realizar este cambio, debes ubicar el archivo web.py y buscar la línea donde se encuentra la dirección "localhost". En lugar de dejarla así, tendrás que modificarla manualmente para reemplazar "localhost" con tu dirección IP pública. Esto permitirá que tu aplicación se comunique correctamente con otros dispositivos en la red.

Además, se recomienda utilizar direcciones IP elásticas. Las direcciones IP elásticas son direcciones IP asignadas a instancias en la nube que pueden persistir incluso si se reinicia la instancia. Esto es importante porque las direcciones IP pueden cambiar cada vez que reinicies tu instancia en la nube. Al utilizar direcciones IP elásticas, te aseguras de que tu aplicación siempre esté disponible y accesible a través de la misma dirección IP, sin importar los reinicios o cambios en la infraestructura de la nube.

Haciendo estos ajustes y utilizando direcciones IP elásticas, garantizarás un correcto funcionamiento de tu aplicación en la nube y facilitarás el acceso a la misma desde otros dispositivos conectados a Internet.

# puertos que se deben habilitar 
![image](https://github.com/jsam2001/telematica/assets/133801550/14014a1f-ae96-4c3d-85c9-bfa2a8cc825d)
# ejecutar inicio.sh 
Este script se encargará de actualizar el repositorio de paquetes y luego instalar Docker Compose, junto con dos imágenes específicas: MySQL y Ubuntu. Finalmente, ejecutará el archivo docker-compose.yml, el cual creará tres contenedores distintos.

El proceso comenzará actualizando el repositorio de paquetes, lo cual es importante para asegurarse de tener acceso a las últimas versiones de los paquetes disponibles. Luego, procederá a instalar Docker Compose, que es una herramienta que permite definir y administrar aplicaciones multi-contenedor de manera sencilla.

Una vez que Docker Compose esté instalado, se procederá a descargar las imágenes necesarias para los contenedores. En este caso, se utilizarán las imágenes de MySQL y Ubuntu. La imagen de MySQL proporcionará una base de datos lista para usar, mientras que la imagen de Ubuntu permitirá trabajar con un sistema operativo Linux.

Por último, se ejecutará el archivo docker-compose.yml. Este archivo es una configuración que describe cómo se deben crear y configurar los contenedores. Al ejecutarlo, se iniciarán los tres contenedores según lo especificado en el archivo, lo que te permitirá utilizar y trabajar con las aplicaciones y servicios proporcionados por cada uno de ellos.

 sudo sh ./inicio.sh
 
 # Para otros sistemas operativos
 
 Si estás utilizando un sistema operativo diferente, necesitarás descargar manualmente Docker Compose, así como las imágenes de MySQL y Ubuntu. Luego, podrás ejecutar el archivo docker-compose.yml para crear los tres contenedores correspondientes.

En primer lugar, deberás descargar Docker Compose específico para tu sistema operativo. Puedes encontrar las instrucciones de instalación en el sitio web oficial de Docker. Sigue los pasos proporcionados para descargar e instalar Docker Compose en tu sistema.

Una vez que Docker Compose esté instalado, deberás descargar manualmente las imágenes de MySQL y Ubuntu. Puedes hacer esto utilizando el comando `docker pull` seguido del nombre de la imagen que deseas descargar. Por ejemplo, puedes ejecutar `docker pull mysql` para obtener la imagen de MySQL y `docker pull ubuntu` para obtener la imagen de Ubuntu.

Una vez que hayas descargado las imágenes, estarás listo para ejecutar el archivo docker-compose.yml. Este archivo contiene la configuración para crear y configurar los contenedores. Utiliza el comando `docker-compose up` en el directorio donde se encuentra el archivo docker-compose.yml para iniciar los contenedores según lo especificado en el archivo.

# final
Después de ejecutar el archivo docker-compose.yml, es necesario esperar un momento hasta que los tres contenedores estén funcionando correctamente. Puedes verificar el estado de los contenedores ejecutando el comando `docker ps` en tu terminal. Espera hasta que veas que los tres contenedores están en estado "running" (corriendo) y listos para su uso.

Una vez que los contenedores estén en funcionamiento, podrás acceder a la aplicación desde tu host local o dirección IP pública a través del puerto 8080. Abre tu navegador web y escribe la dirección "localhost:8080" o tu dirección IP pública seguida de ":8080" en la barra de direcciones. Esto te llevará a la interfaz de la aplicación que se encuentra en ejecución en los contenedores.

Si esta es tu primera vez utilizando la aplicación, deberás registrarte primero antes de poder acceder. Sigue las instrucciones proporcionadas en la interfaz para completar el proceso de registro. Una vez registrado, podrás iniciar sesión y acceder a todas las funcionalidades de la aplicación.

Recuerda que es importante esperar a que los contenedores estén en funcionamiento antes de intentar acceder a la aplicación, ya que esto garantiza un entorno estable y listo para su uso.

De esta manera, podrás utilizar Docker Compose y las imágenes de MySQL y Ubuntu en tu sistema operativo, creando los contenedores necesarios para tu aplicación mediante la ejecución del archivo docker-compose.yml.
