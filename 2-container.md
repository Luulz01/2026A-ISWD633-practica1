# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
<img width="686" height="82" alt="{D0C84AF9-FE5A-410E-B796-7719CB1D9C79}" src="https://github.com/user-attachments/assets/48f397f2-17b2-4503-a118-27e886a5f670" />

# COMPLETAR

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

<img width="628" height="58" alt="{57EB3C64-AE20-4BE8-ADF8-420D97EB29E6}" src="https://github.com/user-attachments/assets/490eb0e0-cb58-42cb-a26d-7737c8daaac4" />

# COMPLETAR

### Listar los contenedores ejecutándose o no

```
docker ps -a
```
<img width="1110" height="139" alt="{3EE998AB-C6A2-4E99-BD67-B14AFF334B69}" src="https://github.com/user-attachments/assets/4a2cc481-ca08-4635-a154-c66daef8738c" />


### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web

<img width="556" height="90" alt="{2F918935-AFD0-4C32-AFF0-537A68C53C9B}" src="https://github.com/user-attachments/assets/2901baf2-955f-40c6-b789-40375744e7d4" />

# COMPLETAR

### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```
docker ps
<img width="1016" height="83" alt="{9C5D3079-11D7-4F8A-813C-4DB975A765F9}" src="https://github.com/user-attachments/assets/889a9a3d-2341-4b43-82e7-6900f3b2cadc" />

docker ps | find "srv-web"
<img width="1066" height="59" alt="{6C17B9B4-2F6B-474F-9FDD-D5FFED4EF167}" src="https://github.com/user-attachments/assets/7f2d1f0b-fdd2-4ae4-850f-359ecab582c1" />

### Para detener un contenedor

```
docker stop <nombre contenedor>
```
<img width="390" height="63" alt="{22192133-D462-4D61-9229-0B9689F25640}" src="https://github.com/user-attachments/assets/38558177-9fae-4611-b374-56b62d2f43f5" />

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
<img width="971" height="517" alt="{0EC67F44-7720-4C6B-86E3-CB72FD1A81B5}" src="https://github.com/user-attachments/assets/d72a4ed1-03ed-4aea-8aea-94728e59b69d" />

# COMPLETAR

**¿Qué sucede luego de la ejecución del comando?**

El comando crea y ejecuta un contenedor llamado srv-web2 con la imagen nginx:alpine. Luego se inicia el servidor nginx en primer plano, mostrando su salida en la terminal, debido a que, la terminal queda como si estuviera ejecutando un proceso, es decir ocupada.
# COMPLETAR  

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

<img width="638" height="98" alt="{E59B89C9-A807-4BA9-B8E9-3BEA8EFDDA6B}" src="https://github.com/user-attachments/assets/fa89a928-31bc-49cd-af25-f70d30d72d71" />

# COMPLETAR

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 

<img width="1219" height="198" alt="{8BB753B5-7DCE-4309-A9C3-A4D3D14815B0}" src="https://github.com/user-attachments/assets/ea808e2e-9236-4ea2-884a-5d7be8f14a53" />

# COMPLETAR

Verificar que el contenedor que se eliminó

<img width="1195" height="143" alt="{9B85577E-4201-4A84-91DD-C3A860125DDD}" src="https://github.com/user-attachments/assets/3c473069-c6f2-40b9-975d-abd8c58a33e9" />

# COMPLETAR

### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

<img width="423" height="68" alt="{AA7E9C52-1BED-4830-B05A-7E120A36CB11}" src="https://github.com/user-attachments/assets/d133e939-4af3-4e5d-a466-bbe67ecf2e92" />

# COMPLETAR

Verificar que el contenedor que se eliminó

<img width="1109" height="103" alt="{A1EC973F-A536-49FB-8348-358E1E3DDFD4}" src="https://github.com/user-attachments/assets/e5698822-079e-40d5-a0d1-4f018826f4d6" />

# COMPLETAR

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 

<img width="1920" height="1080" alt="image" src="https://github.com/user-attachments/assets/e7fbbba6-0301-488b-b602-0fef5576ce9c" />

# COMPLETAR
