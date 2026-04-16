<img width="1013" height="964" alt="{8795A605-DE9A-44A4-92CC-1A22AEEACA77}" src="https://github.com/user-attachments/assets/78fb3b3a-da54-4dff-8de3-66cd249bd62b" /><img width="1094" height="642" alt="{602E7638-6B19-4E29-A5E6-1DF101BC421D}" src="https://github.com/user-attachments/assets/d28f3c80-e09d-4253-8ba1-f5c529e980d1" /># Imagen
### Descargar imagen
Descarga la última versión de la imagen disponible en el registro de Docker.

```
docker pull <nombre imagen> 
```

Descarga una versión específica de la imagen, cada imagen tiene etiquetas (tags) para diferentes versiones.
Una imagen puede tener la etiqueta latest para representar la última versión, si no se especifica una etiqueta se hará referencia a la versión latest.

```
docker pull <nombre imagen>:<tag>
```

Descargar la imagen **hello-world**
# COMPLETAR

**¿Qué es nginx?**
Nginx es un servidor web y proxy de código abierto diseñado para funcionar como intermedirario entre aplicaciones web, tambien nos permite balancear la carga al momento de que los servidores esten sobrecargados.

# COMPLETAR 

Descargar la imagen  **nginx** en la versión **alpine**
<img width="1194" height="566" alt="{2D4FAD7B-2553-4565-AF1E-27C0BE3AB719}" src="https://github.com/user-attachments/assets/815fe945-6921-42f1-a300-5befa092e6cd" />

# COMPLETAR

### Listar imágenes

```
docker images

```

# COLOCAR UNA CAPTURA DE PANTALLA DEL RESULTADO 
<img width="1146" height="170" alt="{9BB4F95C-9769-4E5A-AC52-6CC9F63CC8F6}" src="https://github.com/user-attachments/assets/c0ecc5e7-34ad-4ca0-a612-65c7b9a25e3e" />

**Identificadores**

En Docker, se utilizan varios identificadores para diferenciar de manera única los elementos del sistema, como imágenes, contenedores, volúmenes y redes. Estos identificadores son generados automáticamente por Docker y son únicos dentro del contexto del sistema Docker en el que se encuentran. 

### Inspeccionar una imagen
El comando docker inspect se utiliza para obtener información detallada sobre un objeto de Docker específico, como un contenedor, una imagen, un volumen o una red.  Proporciona información en formato JSON sobre el objeto especificado.

```
docker inspect <nombre imagen>
docker inspect <nombre imagen>:<tag>
```

Inspeccionar la imagen hello-world 
<img width="1013" height="964" alt="{8795A605-DE9A-44A4-92CC-1A22AEEACA77}" src="https://github.com/user-attachments/assets/2718e584-7eb6-4034-95a9-458931bdaab7" />

# COMPLETAR

**¿Con qué algoritmo se está generando el ID de la imagen**

Aplica algortimos de busqueda de hash con un numero acompañado que nos define el tamaño de bits que sea necesario.Docker siempre ocupa SHA-256.

# COMPLETAR

### Filtrar imágenes

```
docker images | grep <termino a buscar>
<img width="1035" height="71" alt="{B24E5299-FDBB-46B4-8E76-6C011244B7F8}" src="https://github.com/user-attachments/assets/8b6b55e0-800a-4e19-af32-f452c19042c1" />

```

### Para eliminar una imagen
Eliminar permanentemente la imagen de tu sistema Docker.

```
docker rmi <nombre imagen>:<tag>
```

Eliminar la imagen hello-world 

<img width="825" height="106" alt="{63A8F972-75CC-491A-BB27-C1CD53FADB84}" src="https://github.com/user-attachments/assets/79aa3d2c-14b9-4d3f-8404-9e41ee2cf478" />

# COMPLETAR

-f: Es la opción para forzar la eliminación de la imagen incluso si hay contenedores en ejecución que utilizan esa imagen.
Cuando eliminas una imagen Docker, Docker no elimina automáticamente los contenedores que se han creado a partir de esa imagen. Esto significa que, aunque hayas eliminado la imagen, el contenedor seguirá ejecutándose normalmente.  
**Considerar**
Eliminar una imagen no afecta a los contenedores que se han creado a partir de esa imagen, a menos que esos contenedores dependan de archivos o configuraciones específicas de la imagen eliminada. En ese caso, es posible que los contenedores se comporten de manera inesperada después de eliminar la imagen.
Es una buena práctica detener y eliminar todos los contenedores que dependan de una imagen antes de eliminar la imagen en sí.

```
docker rmi -f <nombre imagen>:<tag>
```
