# Mi aprendizaje

En esta práctica aprendí sobre Docker que es una plataforma que permite crear, ejecutar y gestionar contenedores, los cuales sirven para ejecutar aplicaciones en entornos aislados, que permite que una aplicación funcione de la misma manera en cualquier computadora sin importar el sistema operativo o configuración. También aprendí qué es una imagen, la cual es una especie de plantilla o base que contiene todo lo necesario para ejecutar una aplicación, como el sistema, librerías y configuraciones. Con conocimiento de eso, se empezó esta práctica desde la descarga de imágenes, creación de contenedores y mapear puertos. 

### **Comandos**

Se presentan los comandos que se utilizaron a lo largo de esta práctica.

**Aplicados en imagen**

- **docker pull `<imagen>`:**  
  Permite descargar una imagen desde Docker Hub.

- **docker pull `<imagen>:<tag>`:**  
  Descarga una versión específica de una imagen.

- **docker images:**  
  Lista todas las imágenes descargadas en el sistema.

- **docker inspect `<imagen>`:**  
  Muestra información detallada de una imagen en formato JSON.

- **docker rmi `<imagen>:<tag>`:**  
  Elimina una imagen del sistema.

- **docker rmi -f `<imagen>`:**  
  Elimina una imagen de forma forzada.

**Aplicados en contenedores**

- **docker create --name `<nombre contenedor>` `<imagen>:<tag>`:**  
  Crea un contenedor sin ejecutarlo.

- **docker start `<nombre contenedor>`:**  
  Inicia un contenedor.

- **docker stop `<nombre contenedor>`:**  
  Detiene un contenedor.

- **docker ps:**  
  Lista los contenedores en ejecución.

- **docker ps -a:**  
  Lista todos los contenedores activos y detenidos.

- **docker run --name `<nombre contenedor>` `<imagen>:<tag>`:**  
  Crea y ejecuta un contenedor.

- **docker run -d --name `<nombre contenedor>` `<imagen>:<tag>`:**  
  Ejecuta un contenedor en segundo plano.

- **docker rm `<nombre contenedor>`:**  
  Elimina un contenedor detenido.

- **docker rm -f `<nombre contenedor>`:**  
  Elimina un contenedor en ejecución de forma forzada.
  
- **docker exec -i `<contenedor>` `<comando>`:**  
  Ejecuta un comando manteniendo la entrada activa.

- **docker exec -it `<contenedor>` bash:**  
  Permite ingresar al contenedor asignandole una terminal.

- **docker logs `<contenedor>`:**  
  Muestra los logs del contenedor.

- **docker logs -n `<número>` `<contenedor>`:**  
  Muestra una cantidad específica de líneas del log.

**Aplicados para mapeo de puertos**

- **docker run -d -p `<host>`:`<contenedor>` `<imagen>`:**  
  Permite acceder a un servicio del contenedor desde el host.

- **docker run -d -p `<host1>`:`<cont1>` -p `<host2>`:`<cont2>` `<imagen>`:**  
  Mapea múltiples puertos.


