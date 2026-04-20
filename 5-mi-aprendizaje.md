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

- **docker run -d --name `<nombre contenedor>` -p `<puerto host>:<puerto contenedor>` `<nombre imagen>:<tag>` :**

  Permite asignar puertos al contenedor para poder mapearlo.

- **docker run -P -d --name `<nombre contenedor>` `<nombre imagen>:<tag>` :**
  
  Le indica a Docker que asigne automáticamente puertos aleatorios en tu host para todos los puertos expuestos por el contenedor.

### Cosas que realicé y aprendí
- Mediante el comando docker pull, descargué imágenes como hello-world y nginx, comprendiendo además el uso de etiquetas (tags) para definir versiones específicas.
- También entendí que los identificadores de las imágenes se generan mediante algoritmos hash como SHA-256, lo que garantiza que cada imagen sea única.
- Aprendí que se puede asignar un nombre a un contenedor o dejar que Docker genere uno automáticamente.
- Observé que cuando se ejecuta sin la opción -d, la terminal queda ocupada, mientras que al usar el modo detach puedo seguir trabajando normalmente.
- En cuanto al mapeo de puertos, comprendí cómo conectar los servicios de un contenedor con mi máquina local utilizando la opción -p.
- Ejecuté comandos como ls -l, whoami y echo, y acceder a archivos internos como la contraseña inicial de Jenkins.

### Conclusión

Finalmente, durante toda la práctica reforcé mi aprendizaje mediante la evidencia visual, colocando capturas de pantalla en cada paso realizado. Estas capturas me ayudaron a verificar que los comandos se ejecutaron correctamente. En conclusión, esta práctica me permitió comprender qué es Docker, cómo funcionan las imágenes y los contenedores, y la importancia para la creación de entornos aislados, portables y eficientes.
