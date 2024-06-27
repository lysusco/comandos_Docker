# comandos_Docker

**Comando 1:**

**Título:** `$ docker run hello-world`

**Descripción:** Ejecuta el contenedor hello-world.

**Función:** Inicia y ejecuta un contenedor que muestra un mensaje de prueba para verificar la instalación correcta de Docker.
---
**Comando 2:**

**Título:** `$ docker ps`

**Descripción:** Muestra los contenedores activos.

**Función:** Lista los contenedores que están actualmente en ejecución.
---
**Comando 3:**

**Título:** `$ docker ps -a`

**Descripción:** Muestra todos los contenedores.

**Función:** Lista todos los contenedores, incluidos los que están parados.
---
**Comando 4:**

**Título:** `$ docker inspect <container ID>`

**Descripción:** Muestra el detalle completo de un contenedor.

**Función:** Proporciona información detallada sobre un contenedor específico identificado por su ID.
---
**Comando 5:**

**Título:** `$ docker inspect <name>`

**Descripción:** Muestra el detalle completo de un contenedor.

**Función:** Proporciona información detallada sobre un contenedor específico identificado por su nombre.
---
**Comando 6:**

**Título:** `$ docker run --name hello-platzi hello-world`

**Descripción:** Le asigno un nombre custom "hello-platzi".

**Función:** Ejecuta el contenedor hello-world asignándole un nombre personalizado "hello-platzi".
---
**Comando 7:**

**Título:** `$ docker rename hello-platzi hola-platzy`

**Descripción:** Cambio el nombre de hello-platzi a hola-platzy.

**Función:** Renombra el contenedor "hello-platzi" a "hola-platzy".
---
**Comando 8:**

**Título:** `$ docker rm <ID o nombre>`

**Descripción:** Borro un contenedor.

**Función:** Elimina un contenedor específico identificado por su ID o nombre.
---
**Comando 9:**

**Título:** `$ docker container prune`

**Descripción:** Borro todos los contenedores que estén parados.

**Función:** Elimina todos los contenedores que no están en ejecución (parados).
**Comando 10:**

**Título:** `$ docker run ubuntu`

**Descripción:** Corre un contenedor de Ubuntu pero lo deja apagado.

**Función:** Inicia un contenedor basado en la imagen de Ubuntu, pero no abre ninguna sesión interactiva ni ejecuta ningún comando específico que mantenga el contenedor en ejecución después de iniciarse.
---
**Comando 11:**

**Título:** `$ docker ps -a`

**Descripción:** Lista todos los contenedores.

**Función:** Muestra todos los contenedores Docker, tanto los activos como los inactivos (parados).
---
**Comando 12:**

**Título:** `$ docker run -it ubuntu`

**Descripción:** Lo corre y entro al shell de Ubuntu.

**Función:** Inicia un contenedor interactivo de Ubuntu y abre una sesión de terminal interactiva dentro de él.
---
**Ejecución en el shell interactivo de Ubuntu:**

**Comando 13:**

**Título:** `cat /etc/lsb-release`

**Descripción:** Veo la versión de Linux.

**Función:** Muestra el contenido del archivo `/etc/lsb-release`, el cual contiene información sobre la distribución Linux específica que se está utilizando dentro del contenedor Ubuntu.
**Comando 14:**

**Título:** `$ docker ps -a`

**Descripción:** Veo todos los contenedores.

**Función:** Lista todos los contenedores Docker, incluidos los que están en ejecución y los detenidos.
---
**Comando 15:**

**Título:** `$ docker --name <nombre> -d ubuntu -f <comando>`

**Descripción:** No es un comando válido de Docker según la sintaxis estándar.

**Función:** No se puede proporcionar una descripción precisa porque el comando está incompleto o incorrecto.
---
**Comando 16:**

**Título:** `$ docker --name alwaysup -d ubuntu tail -f /dev/null`

**Descripción:** Mantiene el contenedor activo.

**Función:** Inicia un contenedor de Ubuntu en segundo plano (`-d`), nombrado como `alwaysup` (`--name alwaysup`). Utiliza `tail -f /dev/null` como un comando que no hace nada pero mantiene el contenedor en ejecución.
---
**Comando 17:**

**Título:** `$ docker exec -it alwaysup bash`

**Descripción:** Entro al contenedor.

**Función:** Abre una sesión interactiva (`-it`) dentro del contenedor `alwaysup` y ejecuta el shell bash.
---
**Comando 18:**

**Título:** `$ docker inspect --format '{{.State.Pid}}' alwaysup`

**Descripción:** Veo el main process del Ubuntu.

**Función:** Utiliza el comando `docker inspect` para obtener el ID del proceso principal (`Pid`) dentro del contenedor llamado `alwaysup`. Este comando específico está formateado para mostrar solo el PID del estado del contenedor.
---
**Desde Linux:**

Si ejecuto `kill -9 <PID>`, mata el proceso dentro del contenedor de Ubuntu.

**Desde macOS:**

No funciona correctamente para matar el proceso dentro del contenedor de Ubuntu debido a diferencias en la implementación de Docker en macOS.
**Comando 19:**

**Título:** `$ docker run -d --name proxy nginx`

**Descripción:** Corro un nginx.

**Función:** Inicia un contenedor Docker en segundo plano (`-d`) utilizando la imagen de nginx y lo nombra como `proxy` (`--name proxy`).
---
**Comando 20:**

**Título:** `$ docker stop proxy`

**Descripción:** Apaga el contenedor.

**Función:** Detiene el contenedor Docker nombrado `proxy`.
---
**Comando 21:**

**Título:** `$ docker rm proxy`

**Descripción:** Borro el contenedor.

**Función:** Elimina definitivamente el contenedor Docker llamado `proxy`.
---
**Comando 22:**

**Título:** `$ docker rm -f <contenedor>`

**Descripción:** Lo para y lo borra.

**Función:** Detiene (`-f` forzadamente) y elimina el contenedor Docker especificado por su nombre o ID.
---
**Comando 23:**

**Título:** `$ docker run -d --name proxy -p 8080:80 nginx`

**Descripción:** Corro un nginx y expongo el puerto 80 del contenedor en el puerto 8080 de mi máquina.

**Función:** Inicia un contenedor Docker en segundo plano (`-d`) utilizando la imagen de nginx, lo nombra como `proxy` (`--name proxy`) y mapea el puerto 80 del contenedor al puerto 8080 de la máquina host (`-p 8080:80`).
---
**Verificación desde el navegador:**

**URL:** `http://localhost:8080`

**Descripción:** Desde mi navegador compruebo que funcione.

**Función:** Accede al servidor nginx ejecutándose en el contenedor a través del puerto 8080 de localhost para verificar que el servicio esté activo y funcione correctamente.
---
**Comando 24:**

**Título:** `$ docker logs proxy`

**Descripción:** Veo los logs.

**Función:** Muestra los logs del contenedor Docker llamado `proxy`.
---
**Comando 25:**

**Título:** `$ docker logs -f proxy`

**Descripción:** Hago un follow del log.

**Función:** Sigue en tiempo real (`-f`) los logs del contenedor Docker llamado `proxy`.
---
**Comando 26:**

**Título:** `$ docker logs --tail 10 -f proxy`

**Descripción:** Veo y sigo solo las 10 últimas entradas del log.

**Función:** Sigue en tiempo real (`-f`) y muestra solo las últimas 10 líneas (`--tail 10`) de los logs del contenedor Docker llamado `proxy`.
**Comando 27:**

**Título:** `$ mkdir dockerdata`

**Descripción:** Creo un directorio en mi máquina.

**Función:** Crea un nuevo directorio llamado `dockerdata` en la ruta actual de la máquina donde se ejecutó el comando.
---
**Comando 28:**

**Título:** `$ docker run -d --name db mongo`

**Descripción:** Corro un contenedor de MongoDB.

**Función:** Inicia un contenedor Docker en segundo plano (`-d`) utilizando la imagen de MongoDB (`mongo`) y lo nombra como `db` (`--name db`).
---
**Comando 29:**

**Título:** `$ docker ps`

**Descripción:** Veo los contenedores activos.

**Función:** Lista todos los contenedores Docker que están actualmente en ejecución.
---
**Comando 30:**

**Título:** `$ docker exec -it db bash`

**Descripción:** Entro al bash del contenedor.

**Función:** Abre una sesión interactiva (`-it`) dentro del contenedor `db` y ejecuta el shell bash.
---
**Dentro del contenedor MongoDB:**

**Comando 31:**

**Título:** `mongo`

**Descripción:** Me conecto a la base de datos.

**Función:** Inicia el cliente de MongoDB para conectarse a la base de datos que está corriendo dentro del contenedor.
---
**Comando 32:**

**Título:** `shows dbs`

**Descripción:** Listo las bases de datos.

**Función:** Muestra las bases de datos disponibles en el servidor de MongoDB.
---
**Comando 33:**

**Título:** `use platzi`

**Descripción:** Creo la base de datos `platzi`.

**Función:** Cambia al contexto de la base de datos `platzi` en MongoDB. Si la base de datos no existe, la crea.
---
**Comando 34:**

**Título:** `db.users.insert({"nombre":"guido"})`

**Descripción:** Inserto un nuevo dato en la colección `users`.

**Función:** Inserta un documento con el campo `"nombre"` con valor `"guido"` en la colección `users` de la base de datos actual (`platzi`).
---
**Comando 35:**

**Título:** `db.users.find()`

**Descripción:** Veo el dato que cargué.

**Función:** Busca y muestra todos los documentos de la colección `users` en la base de datos actual (`platzi`).
---
**Comando 36:**

**Título:** `$ docker run -d --name db -v <path de mi maquina>:<path dentro del contenedor> mongo`

**Descripción:** Corro un contenedor de MongoDB y creo un bind mount.

**Función:** Inicia un nuevo contenedor Docker en segundo plano (`-d`) utilizando la imagen de MongoDB (`mongo`). Utiliza la opción `-v` para montar un directorio (`<path de mi maquina>`) de la máquina host dentro del contenedor en un directorio específico (`<path dentro del contenedor>`, por ejemplo `/data/db`) para almacenar los datos de MongoDB.
**Comando 37:**

**Título:** `$ docker volume ls`

**Descripción:** Listo los volúmenes.

**Función:** Muestra una lista de todos los volúmenes Docker disponibles en el sistema.
---
**Comando 38:**

**Título:** `$ docker volume create dbdata`

**Descripción:** Creo un volumen.

**Función:** Crea un nuevo volumen Docker llamado `dbdata` que puede ser utilizado por contenedores para persistir datos.
---
**Comando 39:**

**Título:** `$ docker run -d --name db --mount src=dbdata,dst=/data/db mongo`

**Descripción:** Corro la base de datos y monto el volumen.

**Función:** Inicia un contenedor Docker en segundo plano (`-d`) utilizando la imagen de MongoDB (`mongo`). Utiliza `--mount` para montar el volumen `dbdata` (`src=dbdata`) en el directorio `/data/db` dentro del contenedor (`dst=/data/db`). Esto permite que MongoDB persista sus datos en el volumen `dbdata`.
---
**Comando 40:**

**Título:** `$ docker inspect db`

**Descripción:** Veo la información detallada del contenedor.

**Función:** Utiliza `docker inspect` para obtener detalles completos y específicos del contenedor Docker llamado `db`, incluyendo configuraciones de red, variables de entorno, volúmenes montados, entre otros.
---
**Comando 41:**

**Título:** `mongo`

**Descripción:** Me conecto a la base de datos.

**Función:** Inicia el cliente de MongoDB para conectarse al servidor de base de datos que está corriendo dentro del contenedor `db`.
---
**Dentro del cliente de MongoDB:**

**Comando 42:**

**Título:** `shows dbs`

**Descripción:** Listo las bases de datos.

**Función:** Muestra las bases de datos disponibles en el servidor de MongoDB.
---
**Comando 43:**

**Título:** `use platzi`

**Descripción:** Creo la base de datos `platzi`.

**Función:** Cambia al contexto de la base de datos `platzi` en MongoDB. Si la base de datos no existe, la crea.
---
**Comando 44:**

**Título:** `db.users.insert({"nombre":"guido"})`

**Descripción:** Inserto un nuevo dato en la colección `users`.

**Función:** Inserta un documento con el campo `"nombre"` con valor `"guido"` en la colección `users` de la base de datos actual (`platzi`).
---
**Comando 45:**

**Título:** `db.users.find()`

**Descripción:** Veo el dato que cargué.

**Función:** Busca y muestra todos los documentos de la colección `users` en la base de datos actual (`platzi`).
**Comando 46:**

**Título:** `$ touch prueba.txt`

**Descripción:** Creo un archivo en mi máquina.

**Función:** Crea un archivo vacío llamado `prueba.txt` en el directorio actual de la máquina donde se ejecutó el comando.
---
**Comando 47:**

**Título:** `$ docker run -d --name copytest ubuntu tail -f /dev/null`

**Descripción:** Corro un contenedor Ubuntu y le agrego `tail -f /dev/null` para que quede activo.

**Función:** Inicia un contenedor Docker en segundo plano (`-d`) utilizando la imagen de Ubuntu (`ubuntu`). Le asigna el nombre `copytest` (`--name copytest`). `tail -f /dev/null` es un comando que no hace nada pero mantiene el contenedor en ejecución.
---
**Comando 48:**

**Título:** `$ docker exec -it copytest bash`

**Descripción:** Entro al contenedor.

**Función:** Abre una sesión interactiva (`-it`) dentro del contenedor `copytest` y ejecuta el shell bash.
---
**Dentro del contenedor Ubuntu:**

**Comando 49:**

**Título:** `mkdir testing`

**Descripción:** Creo un directorio en el contenedor.

**Función:** Crea un nuevo directorio llamado `testing` dentro del contenedor `copytest`.
---
**Comando 50:**

**Título:** `$ docker cp prueba.txt copytest:/testing/test.txt`

**Descripción:** Copio el archivo dentro del contenedor.

**Función:** Copia el archivo `prueba.txt` desde la máquina host al directorio `/testing/test.txt` dentro del contenedor `copytest`.
---
**Comando 51:**

**Título:** `$ docker cp copytest:/testing localtesting`

**Descripción:** Copio el directorio de un contenedor a mi máquina.

**Función:** Copia el directorio `/testing` desde el contenedor `copytest` a un directorio local llamado `localtesting` en la máquina host. Con `docker cp`, no es necesario que el contenedor esté corriendo para copiar archivos o directorios desde o hacia él.
**Comando 52:**

**Título:** `$ docker image ls`

**Descripción:** Veo las imágenes que tengo localmente.

**Función:** Lista todas las imágenes Docker que están almacenadas localmente en la máquina.
---
**Comando 53:**

**Título:** `$ docker pull ubuntu:20.04`

**Descripción:** Bajo la imagen de Ubuntu con una versión específica.

**Función:** Descarga la imagen de Ubuntu con la etiqueta `20.04` desde Docker Hub si no está presente localmente.
---
Para eliminar una imagen:

**Comando 54:**

**Título:** `$ docker image rm -f {id_image}`

**Descripción:** Elimina una imagen de Docker.

**Función:** Elimina de manera forzada (`-f`) una imagen específica identificada por su ID (`{id_image}`). Es importante tener en cuenta que la eliminación de una imagen es permanente y no se puede deshacer, por lo que se debe realizar con precaución.
Para los comandos proporcionados, aquí está el detalle de cada uno:

**Comando 55:**

**Título:** `$ mkdir imagenes`

**Descripción:** Creo un directorio en mi máquina.

**Función:** Crea un nuevo directorio llamado `imagenes` en el directorio actual de la máquina donde se ejecutó el comando.
---
**Comando 56:**

**Título:** `$ cd imagenes`

**Descripción:** Entro al directorio.

**Función:** Cambia el directorio de trabajo actual al directorio `imagenes`.
---
**Comando 57:**

**Título:** `$ touch Dockerfile`

**Descripción:** Creo un Dockerfile.

**Función:** Crea un archivo vacío llamado `Dockerfile` dentro del directorio `imagenes`.
---
**Comando 58:**

**Título:** `$ code .`

**Descripción:** Abro VS Code en el directorio en el que estoy.

**Función:** Abre Visual Studio Code (o cualquier otro editor configurado) en el directorio actual (`imagenes`) para trabajar con el contenido del proyecto.
---
**Contenido del Dockerfile:**

```dockerfile
# Contenido del Dockerfile
FROM ubuntu:latest
RUN touch /usr/src/hola-platzi.txt
##fin##
```

**Explicación del Dockerfile:**
- `FROM ubuntu:latest`: Utiliza la imagen base oficial de Ubuntu en su versión más reciente como base.
- `RUN touch /usr/src/hola-platzi.txt`: Ejecuta el comando `touch` durante el proceso de construcción del contenedor para crear un archivo llamado `hola-platzi.txt` en la ruta `/usr/src/` dentro del contenedor.
---
**Comando 59:**

**Título:** `$ docker build -t ubuntu:platzi .`

**Descripción:** Creo una imagen con el contexto de build `<directorio>`.

**Función:** Construye una nueva imagen Docker utilizando el Dockerfile (`Dockerfile`) ubicado en el directorio actual (`.`) y le asigna el tag `-t ubuntu:platzi`.
---
**Comando 60:**

**Título:** `$ docker run -it ubuntu:platzi`

**Descripción:** Corro el contenedor con la nueva imagen.

**Función:** Inicia un contenedor Docker interactivo (`-it`) utilizando la imagen `ubuntu:platzi` que acabamos de construir.
---
**Comando 61:**

**Título:** `$ docker login`

**Descripción:** Me logueo en Docker Hub.

**Función:** Autentica al usuario actual con Docker Hub para poder realizar operaciones como push de imágenes.
---
**Comando 62:**

**Título:** `$ docker tag ubuntu:platzi miusuario/ubuntu:platzy`

**Descripción:** Cambio el tag para poder subirla a mi Docker Hub.

**Función:** Cambia el tag de la imagen local `ubuntu:platzi` a `miusuario/ubuntu:platzy`. Esto prepara la imagen para ser subida y publicada en el repositorio personalizado del usuario en Docker Hub.
---
**Comando 63:**

**Título:** `$ docker push miusuario/ubuntu:platzi`

**Descripción:** Publico la imagen a mi Docker Hub.

**Función:** Sube y publica la imagen local `miusuario/ubuntu:platzi` al repositorio de imágenes en Docker Hub asociado al usuario. Esto permite que la imagen esté disponible públicamente para ser descargada y utilizada por otros usuarios de Docker Hub.
**Comando 64:**

**Título:** `$ docker history ubuntu:platzi`

**Descripción:** Veo la información de cómo se construyó cada capa de la imagen.

**Función:** Muestra un historial detallado de las capas que componen la imagen `ubuntu:platzi`. Cada capa representa un paso en el proceso de construcción de la imagen, mostrando los comandos ejecutados y los cambios realizados en el sistema de archivos en cada etapa.
---
**Comando 65:**

**Título:** `$ dive ubuntu:platzi`

**Descripción:** Veo la información de la imagen con el programa dive.

**Función:** `dive` es una herramienta interactiva de línea de comandos para explorar y analizar imágenes Docker en detalle. Al ejecutar `dive ubuntu:platzi`, se abre una interfaz interactiva que permite visualizar y analizar cada capa de la imagen `ubuntu:platzi`, mostrando información como el tamaño de cada capa, los archivos añadidos o modificados, y proporcionando recomendaciones para optimizar el tamaño de la imagen si es necesario.
Para los comandos proporcionados y la corrección señalada:

**Comando 66:**

**Título:** `$ git clone https://github.com/platzi/docker`

**Descripción:** Clono el repositorio de GitHub `docker` de Platzi.

**Función:** Clona el repositorio `docker` de Platzi desde GitHub en el directorio actual de trabajo en tu máquina local.
---
**Comando 67:**

**Título:** `$ docker build -t platziapp .`

**Descripción:** Creo la imagen local.

**Función:** Construye una imagen Docker utilizando el Dockerfile presente en el directorio actual (`.`) y le asigna el tag `-t platziapp`.
---
**Comando 68:**

**Título:** `$ docker image ls`

**Descripción:** Listo las imágenes locales.

**Función:** Muestra una lista de todas las imágenes Docker que están almacenadas localmente en la máquina.
---
**Comando 69:**

**Título:** `$ docker run --rm -p 3000:3000 platziapp`

**Descripción:** Creo el contenedor y cuando se detenga se borra, lo publica el puerto 3000.

**Función:** Inicia un contenedor Docker utilizando la imagen `platziapp`. La opción `--rm` indica que el contenedor se eliminará automáticamente cuando se detenga. `-p 3000:3000` mapea el puerto `3000` del contenedor al puerto `3000` de la máquina host, permitiendo acceder a la aplicación a través de ese puerto.
---
**Comando 70:**

**Título:** `$ docker ps`

**Descripción:** Veo los contenedores activos.

**Función:** Lista todos los contenedores Docker que están actualmente en ejecución.
---
Estos comandos te permiten clonar un repositorio de GitHub, construir una imagen Docker a partir de un Dockerfile, listar las imágenes locales disponibles, ejecutar un contenedor basado en la imagen construida y verificar los contenedores activos.
Para los comandos proporcionados:

**Comando 71:**

**Título:** `$ docker build -t platziapp .`

**Descripción:** Creo la imagen local.

**Función:** Construye una imagen Docker utilizando el Dockerfile presente en el directorio actual (`.`) y le asigna el tag `-t platziapp`.
---
**Comando 72:**

**Título:** `$ docker run --rm -p 3000:3000 -v pathlocal/index.js:pathcontenedor/index.js platziapp`

**Descripción:** Corro un contenedor y monto el archivo index.js para que se actualice dinámicamente con nodemon que está declarado en mi Dockerfile.

**Función:** 
- `docker run`: Inicia un contenedor Docker.
- `--rm`: Elimina automáticamente el contenedor cuando se detiene.
- `-p 3000:3000`: Mapea el puerto 3000 del contenedor al puerto 3000 de la máquina host.
- `-v pathlocal/index.js:pathcontenedor/index.js`: Monta el archivo `index.js` ubicado en `pathlocal` (en la máquina host) dentro del contenedor en la ruta `pathcontenedor/index.js`. Esto permite que los cambios realizados en `index.js` en la máquina local se reflejen automáticamente dentro del contenedor.
- `platziapp`: Especifica la imagen a partir de la cual se crea el contenedor, en este caso, `platziapp`.

Este comando asume que ya tienes un Dockerfile configurado correctamente para ejecutar una aplicación con `nodemon` o un servicio similar que detecte cambios en `index.js` y reinicie automáticamente la aplicación cuando se detecten cambios.

### Ejemplo de Dockerfile:

```dockerfile
# Dockerfile para una aplicación Node.js con nodemon

# Utiliza una imagen base con Node.js
FROM node:latest

# Establece el directorio de trabajo dentro del contenedor
WORKDIR /app

# Copia los archivos de la aplicación al contenedor
COPY . .

# Instala las dependencias
RUN npm install

# Instala nodemon globalmente para que esté disponible en todo el sistema
RUN npm install -g nodemon

**Comando 73:**
CMD ["nodemon", "index.js"]
```

En este Dockerfile:

- Se copian todos los archivos del directorio actual (donde se encuentra el Dockerfile) al directorio de trabajo `/app` dentro del contenedor.
- Se instalan las dependencias con `npm install`.
- Se instala `nodemon` globalmente para que esté disponible en todo el sistema.
- El comando `CMD ["nodemon", "index.js"]` establece que al iniciar el contenedor, se debe ejecutar la aplicación usando `nodemon`, lo cual permite que la aplicación se reinicie automáticamente cuando se realicen cambios en `index.js`.

Asegúrate de adaptar `index.js` y la estructura de tu aplicación según sea necesario en tu proyecto específico.
Aquí tienes la explicación detallada de cada comando proporcionado:

**Comando 74:**

**Título:** `$ docker network ls`

**Descripción:** Listo las redes.

**Función:** Muestra una lista de todas las redes Docker disponibles en el sistema.
---
**Comando 75:**

**Título:** `$ docker network create --attachable plazinet`

**Descripción:** Creo la red.

**Función:** Crea una nueva red Docker llamada `plazinet` con la opción `--attachable`, lo que permite que los contenedores se conecten y desconecten de esta red de forma dinámica.
---
**Comando 76:**

**Título:** `$ docker inspect plazinet`

**Descripción:** Veo toda la definición de la red creada.

**Función:** Utiliza `docker inspect` para obtener información detallada sobre la red Docker llamada `plazinet`, incluyendo configuraciones de red, contenedores conectados, y más.
---
**Comando 77:**

**Título:** `$ docker run -d --name db mongo`

**Descripción:** Creo el contenedor de la base de datos.

**Función:** Inicia un contenedor Docker en segundo plano (`-d`) utilizando la imagen de MongoDB (`mongo`) y le asigna el nombre `db` (`--name db`).
---
**Comando 78:**

**Título:** `$ docker network connect plazinet db`

**Descripción:** Conecto el contenedor "db" a la red "platzinet".

**Función:** Conecta el contenedor llamado `db` a la red Docker llamada `plazinet`. Esto permite que `db` pueda comunicarse con otros contenedores en la misma red.
---
**Comando 79:**

**Título:** `$ docker run -d --name app -p 3000:3000 --env MONGO_URL=mongodb://db:27017/test platzi`

**Descripción:** Corro el contenedor "app" y le paso una variable.

**Función:** Inicia un contenedor Docker en segundo plano (`-d`) utilizando la imagen `platzi`. Asigna el nombre `app` (`--name app`) y mapea el puerto `3000` del contenedor al puerto `3000` de la máquina host (`-p 3000:3000`). Además, pasa una variable de entorno `MONGO_URL` con el valor `mongodb://db:27017/test`, lo que permite que la aplicación dentro del contenedor se conecte a la base de datos MongoDB (`db`) en la red `plazinet`.
---
**Comando 80:**

**Título:** `$ docker network connect plazinet app`

**Descripción:** Conecto el contenedor "app" a la red "plazinet".

**Función:** Conecta el contenedor llamado `app` a la red Docker llamada `plazinet`. Esto facilita la comunicación entre los contenedores `app` y `db` a través de la red definida, permitiendo que la aplicación acceda a la base de datos MongoDB (`db`) mediante el nombre de servicio `db` dentro de la red `plazinet`.

Estos comandos muestran cómo crear redes Docker, conectar contenedores a estas redes y configurar la comunicación entre contenedores utilizando variables de entorno para configuraciones específicas, como la URL de conexión a la base de datos MongoDB.
El comando `$ docker-compose up -d` es utilizado para levantar todos los servicios definidos en un archivo `docker-compose.yml` en modo detached (en segundo plano). Aquí está la explicación detallada:

**Comando 81:**

**Título:** `$ docker-compose up -d`

**Descripción:** Crea todo lo declarado en el archivo docker-compose.yml.

**Función:** 
- `docker-compose up`: Este comando levanta todos los servicios definidos en el archivo `docker-compose.yml`. 
- `-d` (o `--detach`): Esta bandera indica que los contenedores deben ejecutarse en segundo plano, es decir, de manera detached.

### Explicación detallada:

1. **docker-compose.yml:** Este es un archivo YAML donde se definen los servicios que componen tu aplicación. En este archivo, se especifican las imágenes de Docker que se utilizarán, las redes, volúmenes, variables de entorno y cualquier otra configuración necesaria para cada servicio.

2. **`docker-compose up`:**
   - **Levanta los servicios:** Ejecuta los contenedores según las configuraciones especificadas en el archivo `docker-compose.yml`.
   - **Construcción automática:** Si las imágenes de los servicios no existen localmente, `docker-compose` las construirá automáticamente utilizando los Dockerfiles en los directorios de cada servicio.
   - **Inicio en segundo plano (`-d`):** La opción `-d` asegura que los contenedores se ejecuten en segundo plano, lo que significa que no bloquearán la terminal desde la cual se lanzó el comando.

3. **Beneficios:**
   - **Orquestación simplificada:** `docker-compose` simplifica la gestión de múltiples contenedores, permitiendo definir la configuración de todos los servicios en un solo archivo.
   - **Interconexión automática:** Los servicios definidos en el mismo archivo `docker-compose.yml` pueden comunicarse entre sí mediante sus nombres de servicio, facilitando la configuración de redes y la gestión de dependencias.

4. **Uso común:**
   - Este comando es ampliamente utilizado en entornos de desarrollo y despliegue para levantar aplicaciones complejas que constan de múltiples servicios interrelacionados, como bases de datos, servidores web, servicios backend, etc.

Al ejecutar `docker-compose up -d`, asegúrate de estar en el directorio que contiene tu archivo `docker-compose.yml`, ya que `docker-compose` buscará este archivo en el directorio actual por defecto.
Aquí tienes la explicación detallada de cada comando proporcionado relacionado con Docker y Docker Compose:

**Comando 82:**

**Título:** `$ docker network ls`

**Descripción:** Listo las redes.

**Función:** Muestra una lista de todas las redes Docker disponibles en el sistema.
---
**Comando 83:**

**Título:** `$ docker network inspect docker_default`

**Descripción:** Veo la definición de la red.

**Función:** Utiliza `docker network inspect` para obtener información detallada sobre la red Docker llamada `docker_default`, incluyendo configuraciones de red, contenedores conectados, y más.
---
**Comando 84:**

**Título:** `$ docker-compose logs`

**Descripción:** Veo todos los logs.

**Función:** Muestra los logs de todos los servicios definidos en el archivo `docker-compose.yml`. Esto incluye logs de todos los contenedores que están siendo administrados por Docker Compose.
---
**Comando 85:**

**Título:** `$ docker-compose logs app`

**Descripción:** Solo veo el log de "app".

**Función:** Muestra los logs específicamente del servicio llamado `app` definido en el archivo `docker-compose.yml`. Esto es útil para enfocarse en los logs de un servicio particular dentro de una aplicación multi-servicio.
---
**Comando 86:**

**Título:** `$ docker-compose logs -f app`

**Descripción:** Hago un follow del log de app.

**Función:** Realiza un seguimiento continuo (follow) de los logs del servicio `app`. Muestra los nuevos logs a medida que se generan en tiempo real. Es útil para monitorear el comportamiento o depuración de un servicio específico mientras está en ejecución.
---
**Comando 87:**

**Título:** `$ docker-compose exec app bash`

**Descripción:** Entro al shell del contenedor app.

**Función:** Inicia una sesión interactiva en el shell (`bash`) del contenedor `app` definido en el archivo `docker-compose.yml`. Esto te permite ejecutar comandos dentro del contenedor, realizar pruebas, o diagnosticar problemas directamente desde el shell del contenedor.
---
**Comando 88:**

**Título:** `$ docker-compose ps`

**Descripción:** Veo los contenedores generados por Docker Compose.

**Función:** Muestra el estado actual de todos los servicios definidos en el archivo `docker-compose.yml`. Proporciona información sobre el estado de ejecución (en ejecución o detenido), los puertos mapeados y otros detalles relevantes de los contenedores.
---
**Comando 89:**

**Título:** `$ docker-compose down`

**Descripción:** Borro todo lo generado por Docker Compose.

**Función:** Detiene y elimina todos los contenedores, redes y volúmenes que fueron creados por Docker Compose según la configuración en el archivo `docker-compose.yml`. Es utilizado para limpiar el entorno de desarrollo o pruebas después de terminar de trabajar con la aplicación.
---
Estos comandos son esenciales para gestionar y administrar aplicaciones multi-contenedor utilizando Docker Compose, facilitando tareas como monitoreo de logs, acceso a shells de contenedores, y gestión de redes y contenedores de manera eficiente.
Aquí tienes la explicación detallada de cada comando proporcionado relacionado con Docker Compose:

**Comando 90:**

**Título:** `$ docker-compose build`

**Descripción:** Crea las imágenes.

**Función:** Este comando construye las imágenes de Docker para todos los servicios definidos en el archivo `docker-compose.yml`. Utiliza los Dockerfiles y contextos de build especificados en cada servicio para generar las imágenes necesarias para los contenedores.
---
**Comando 91:**

**Título:** `$ docker-compose up -d`

**Descripción:** Crea los servicios/contenedores.

**Función:** `docker-compose up` levanta todos los servicios definidos en el archivo `docker-compose.yml`. La opción `-d` (o `--detach`) indica que los contenedores deben ejecutarse en segundo plano, es decir, de manera detached.

- **Creación de servicios:** Inicia todos los contenedores según la configuración especificada en `docker-compose.yml`.
- **Interacción con redes y volúmenes:** Conecta los contenedores a las redes definidas y monta los volúmenes necesarios según la configuración.
- **Mapeo de puertos:** Realiza los mapeos de puertos definidos en `docker-compose.yml`, permitiendo acceder a los servicios a través de los puertos especificados en el host.
---
**Comando 92:**

**Título:** `$ docker-compose logs app`

**Descripción:** Veo los logs de "app".

**Función:** Muestra los logs del servicio `app` específicamente, que está definido en el archivo `docker-compose.yml`. Esto incluye todos los registros generados por el contenedor `app` desde su inicio hasta el momento actual.
---
**Comando 93:**

**Título:** `$ docker-compose logs -f app`

**Descripción:** Hago un follow de los logs de "app".

**Función:** Realiza un seguimiento continuo (follow) de los logs del servicio `app`. Muestra los nuevos logs a medida que se generan en tiempo real. Es útil para monitorear el comportamiento de `app` mientras está en ejecución o para depurar problemas que puedan surgir.
---
Estos comandos son fundamentales para trabajar con aplicaciones multi-contenedor utilizando Docker Compose. Permiten construir imágenes, levantar servicios, monitorear logs específicos de servicios y seguir los logs en tiempo real para facilitar la depuración y el monitoreo de aplicaciones.
Aquí tienes la explicación detallada de cada comando proporcionado relacionado con Docker Compose:

**Comando 94:**

**Título:** `$ touch docker-compose.override.yml`

**Descripción:** Creo el archivo override.

**Función:** Este comando crea un archivo `docker-compose.override.yml`. Este archivo se utiliza para sobrescribir o añadir configuraciones adicionales a las definiciones de servicios existentes en el archivo `docker-compose.yml`, sin necesidad de modificar directamente el archivo principal.
---
**Comando 95:**

**Título:** `$ docker-compose up -d`

**Descripción:** Crea los servicios/contenedores.

**Función:** `docker-compose up` levanta todos los servicios definidos en el archivo `docker-compose.yml`. La opción `-d` (o `--detach`) indica que los contenedores deben ejecutarse en segundo plano, es decir, de manera detached.

- **Creación de servicios:** Inicia todos los contenedores según la configuración especificada en `docker-compose.yml` y `docker-compose.override.yml` (si existe).
- **Interacción con redes y volúmenes:** Conecta los contenedores a las redes definidas y monta los volúmenes necesarios según la configuración.
- **Mapeo de puertos:** Realiza los mapeos de puertos definidos en `docker-compose.yml`, permitiendo acceder a los servicios a través de los puertos especificados en el host.
---
**Comando 96:**

**Título:** `$ docker-compose exec app bash`

**Descripción:** Entro al bash del contenedor app.

**Función:** Inicia una sesión interactiva en el shell (`bash`) del contenedor `app` definido en el archivo `docker-compose.yml`. Esto te permite ejecutar comandos dentro del contenedor, realizar pruebas, o diagnosticar problemas directamente desde el shell del contenedor.
---
**Comando 97:**

**Título:** `$ docker-compose ps`

**Descripción:** Veo los contenedores del compose.

**Función:** Muestra el estado actual de todos los servicios definidos en el archivo `docker-compose.yml`. Proporciona información sobre el estado de ejecución (en ejecución o detenido), los puertos mapeados y otros detalles relevantes de los contenedores.
---
**Comando 98:**

**Título:** `$ docker-compose up -d --scale app=2`

**Descripción:** Escalo dos instancias de app, previamente tengo que definir un rango de puertos en el archivo compose.

**Función:** Escala el servicio `app` a dos instancias (`--scale app=2`). Antes de ejecutar este comando, es necesario haber definido un rango de puertos en el archivo `docker-compose.yml` para evitar conflictos de puertos entre las instancias escaladas.

- **Definición de rangos de puertos:** En el archivo `docker-compose.yml`, puedes definir un rango de puertos para cada instancia de `app` utilizando la opción `ports` bajo la configuración del servicio `app`. Por ejemplo: `ports: - "3000-3001:3000"`.
---
**Comando 99:**

**Título:** `$ docker-compose down`

**Descripción:** Borro todo lo creado con compose.

**Función:** Detiene y elimina todos los contenedores, redes y volúmenes que fueron creados por Docker Compose según la configuración en el archivo `docker-compose.yml`. Es utilizado para limpiar el entorno de desarrollo o pruebas después de terminar de trabajar con la aplicación.
---
Estos comandos son útiles para gestionar y administrar aplicaciones multi-contenedor utilizando Docker Compose, facilitando tareas como la gestión de configuraciones adicionales, la interacción con contenedores individuales, el escalado de servicios y la limpieza del entorno después de su uso.
Aquí están las explicaciones de cada comando Docker que mencionaste:

**Comando 100:**

**Título:** `$ docker ps -a`

**Descripción:** Veo todos los contenedores de mi máquina.

**Función:** Muestra una lista de todos los contenedores en el sistema, incluyendo los que están corriendo y los que están detenidos.
---
**Comando 101:**

**Título:** `$ docker container prune`

**Descripción:** Borra todos los contenedores inactivos.

**Función:** Elimina todos los contenedores detenidos, liberando espacio en el sistema y limpiando los recursos que no se están utilizando.
---
**Comando 102:**

**Título:** `$ docker rm -f $(docker ps -aq)`

**Descripción:** Borra todos los contenedores que estén corriendo o apagados.

**Función:** Utiliza `docker ps -aq` para obtener una lista de todos los IDs de contenedores en el sistema y luego utiliza `docker rm -f` para forzar la eliminación de todos esos contenedores, ya sea que estén corriendo o detenidos.
---
**Comando 103:**

**Título:** `$ docker network ls`

**Descripción:** Lista todas las redes.

**Función:** Muestra una lista de todas las redes Docker disponibles en el sistema. Esto incluye las redes predeterminadas y las redes personalizadas que hayas creado.
---
**Comando 104:**

**Título:** `$ docker volume ls`

**Descripción:** Lista todos los volumes.

**Función:** Muestra una lista de todos los volúmenes Docker en el sistema. Los volúmenes son utilizados para persistir datos de contenedores de manera independiente del ciclo de vida del contenedor.
---
**Comando 105:**

**Título:** `$ docker image ls`

**Descripción:** Lista todas las imágenes.

**Función:** Muestra una lista de todas las imágenes Docker disponibles en el sistema. Esto incluye las imágenes base y las imágenes personalizadas que hayas creado o descargado.
---
**Comando 106:**

**Título:** `$ docker system prune`

**Descripción:** Borra todo lo que no se esté usando.

**Función:** Elimina todos los recursos no utilizados en Docker, incluyendo contenedores detenidos, redes no utilizadas, volúmenes sin asociación y más. Es útil para liberar espacio en disco y limpiar recursos innecesarios.
---
**Comando 107:**

**Título:** `$ docker run -d --name app --memory 1g platziapp`

**Descripción:** Limito el uso de memoria.

**Función:** Ejecuta un contenedor llamado `app` a partir de la imagen `platziapp`, limitando su uso de memoria a 1 GB (`--memory 1g`). Esto asegura que el contenedor no consuma más memoria de la especificada, ayudando a controlar los recursos utilizados por los contenedores Docker.
---
**Comando 108:**

**Título:** `$ docker stats`

**Descripción:** Veo cuántos recursos consume Docker en mi sistema.

**Función:** Muestra estadísticas en tiempo real sobre el uso de recursos (CPU, memoria, red, etc.) por parte de todos los contenedores Docker en ejecución en el sistema.
---
**Comando 109:**

**Título:** `$ docker inspect app`

**Descripción:** Puedo ver si el proceso muere por falta de recursos.

**Función:** Utiliza `docker inspect` para obtener información detallada sobre el contenedor llamado `app`. Puedes revisar la configuración de recursos, estado actual y otros detalles para verificar si el contenedor ha tenido problemas relacionados con recursos, como falta de memoria o CPU.
---
Estos comandos son fundamentales para administrar contenedores, redes, volúmenes, imágenes y recursos en Docker, proporcionando herramientas para la gestión eficiente de recursos y la depuración de problemas relacionados con el uso de recursos.
Aquí tienes la explicación de cada comando Docker proporcionado:

**Comando 110:**

**Título:** `$ docker build -t loop .`

**Descripción:** Construyo la imagen.

**Función:** Utiliza `docker build` para construir una imagen Docker a partir de un Dockerfile (`.` indica el contexto actual). La opción `-t loop` etiqueta la imagen resultante con el nombre `loop`.
---
**Comando 111:**

**Título:** `$ docker run -d --name looper loop`

**Descripción:** Corro el contenedor.

**Función:** Utiliza `docker run` para ejecutar un contenedor a partir de la imagen etiquetada como `loop`. La opción `-d` indica que el contenedor debe ejecutarse en segundo plano (detached mode). `--name looper` establece el nombre del contenedor como `looper`.
---
**Comando 112:**

**Título:** `$ docker stop looper`

**Descripción:** Le envía la señal SIGTERM al contenedor.

**Función:** Detiene el contenedor llamado `looper` enviándole una señal SIGTERM. Esta señal permite al contenedor realizar una salida limpia, es decir, finaliza los procesos en curso y luego detiene el contenedor.
---
**Comando 113:**

**Título:** `$ docker ps -l`

**Descripción:** Muestra el ps del último proceso.

**Función:** Utiliza `docker ps -l` para mostrar información del último contenedor que se ejecutó. Esta opción `-l` (o `--latest`) muestra el último contenedor que se ha iniciado, independientemente de su estado actual (corriendo o detenido).
---
**Comando 114:**

**Título:** `$ docker kill looper`

**Descripción:** Le envía la señal SIGKILL al contenedor.

**Función:** Termina abruptamente el contenedor `looper` enviándole una señal SIGKILL. Esta señal fuerza la terminación inmediata del contenedor y sus procesos, sin permitir que realice una salida limpia. Es útil cuando se necesita detener un contenedor rápidamente, pero puede resultar en la pérdida de datos no guardados.
---
**Comando 115:**

**Título:** `$ docker exec looper ps -ef`

**Descripción:** Veo los procesos del contenedor.

**Función:** Utiliza `docker exec` para ejecutar el comando `ps -ef` dentro del contenedor llamado `looper`. Esto muestra una lista detallada de todos los procesos en ejecución dentro del contenedor, proporcionando información como el ID del proceso (PID), el usuario que lo ejecuta, el uso de CPU, etc.
---
Estos comandos son útiles para construir imágenes Docker, manejar contenedores, detenerlos o matarlos, y para revisar los procesos en ejecución dentro de un contenedor específico. Ayudan en el desarrollo, la depuración y la gestión de aplicaciones y servicios basados en contenedores Docker.
Aquí tienes la corrección del comando y la explicación correspondiente:

**Comando 116:**

```bash
$ docker build -t ping .
```

**Título:** Construyo la imagen.

**Descripción:** Utiliza `docker build` para construir una imagen Docker a partir de un Dockerfile en el directorio actual (`.`). La opción `-t ping` etiqueta la imagen resultante con el nombre `ping`.
---
**Comando 117:**

```bash
$ docker run --name pinger ping <hostname>
```

**Título:** Corro el contenedor con parámetro.

**Descripción:** Utiliza `docker run` para ejecutar un contenedor a partir de la imagen etiquetada como `ping`. La opción `--name pinger` establece el nombre del contenedor como `pinger`. `<hostname>` es un parámetro que se pasa al contenedor. Para que esto funcione correctamente, debes haber configurado previamente el `ENTRYPOINT` en el Dockerfile de la imagen `ping`.

**Función del `ENTRYPOINT` en el Dockerfile:**

Para permitir que el contenedor reciba un parámetro y lo procese, debes configurar el `ENTRYPOINT` en el Dockerfile. Aquí hay un ejemplo de cómo podrías hacerlo:

```dockerfile
FROM alpine:latest
ENTRYPOINT ["ping", "-c", "4"]
```

En este ejemplo:

- `FROM alpine:latest`: Usa la imagen base Alpine Linux.
- `ENTRYPOINT ["ping", "-c", "4"]`: Define el comando inicial que se ejecutará cuando el contenedor se inicie. `ping` es el comando principal, y `"-c", "4"` son argumentos opcionales para especificar que se enviarán 4 paquetes de ping.

**Cómo se usa el comando:**

Después de construir la imagen usando `docker build -t ping .`, puedes ejecutar el contenedor con:

```bash
$ docker run --name pinger ping example.com
```

Donde `example.com` es el `<hostname>` que se pasará al comando `ping` configurado en el `ENTRYPOINT`. Esto ejecutará el comando `ping example.com` dentro del contenedor `pinger`, enviando paquetes de ping al host `example.com`.

Este enfoque te permite configurar contenedores Docker para que actúen como herramientas ejecutables que pueden recibir argumentos específicos al iniciarse, facilitando la automatización y la integración con otros sistemas.
Aquí tienes la explicación de cada comando Docker proporcionado:

**Comando 118:**

```bash
$ docker build -t prueba .
```

**Título:** Creo la imagen.

**Descripción:** Utiliza `docker build` para construir una imagen Docker a partir de un Dockerfile en el directorio actual (`.`). La opción `-t prueba` etiqueta la imagen resultante con el nombre `prueba`.
---
**Comando 119:**

```bash
$ docker run -d --rm --name app prueba
```

**Título:** Corro el contenedor.

**Descripción:** Utiliza `docker run` para ejecutar un contenedor a partir de la imagen etiquetada como `prueba`. La opción `-d` indica que el contenedor debe ejecutarse en segundo plano (detached mode). `--rm` especifica que el contenedor debe ser eliminado automáticamente después de que se detenga. `--name app` establece el nombre del contenedor como `app`.
---
**Sobre el archivo `.dockerignore`:**

El archivo `.dockerignore` permite especificar qué archivos y directorios deben ser excluidos del contexto de build cuando se utiliza el comando `docker build`. Esto ayuda a reducir el tamaño del contexto de build y a mejorar la velocidad de construcción de la imagen Docker.

Por ejemplo, si tu archivo `.dockerignore` contiene la línea `logs/`, Docker ignorará todos los archivos y directorios dentro de la carpeta `logs/` cuando construya la imagen. Esto significa que esos archivos no serán copiados dentro del contenedor durante el proceso de construcción de la imagen.
---
**Comando 120:**

```bash
$ docker exec -it app bash
```

**Título:** Entro al contenedor y verifico que no se haya copiado lo que está en el `.dockerignore`.

**Descripción:** Utiliza `docker exec` para ejecutar el comando `bash` dentro del contenedor llamado `app`. La opción `-it` permite la interacción interactiva con el terminal (`i` para interactivo y `t` para asignar un pseudo-TTY).

**Verificación:**

Dentro del contenedor `app`, puedes navegar a los directorios que fueron ignorados en el archivo `.dockerignore` y verificar que los archivos y directorios especificados no se hayan copiado durante la construcción de la imagen. Esto demuestra que el archivo `.dockerignore` ha funcionado correctamente para excluir esos elementos del contexto de build.
Aquí tienes la explicación de los comandos Docker proporcionados:

**Comando 121:**

```bash
$ docker build -t prodapp -f Dockerfile .
```

**Título:** Construyo la imagen especificando el Dockerfile.

**Descripción:** Utiliza `docker build` para construir una imagen Docker a partir de un Dockerfile específico (`-f Dockerfile`). La opción `-t prodapp` etiqueta la imagen resultante con el nombre `prodapp`. El `.` al final especifica el contexto de build actual, es decir, el directorio donde se encuentra el Dockerfile.

**Función:** Este comando es útil cuando tienes múltiples Dockerfiles en un proyecto y necesitas construir una imagen específica utilizando un Dockerfile en particular.
---
**Comando 122:**

```bash
$ docker run -d --name prod prodapp
```

**Título:** Corro el contenedor.

**Descripción:** Utiliza `docker run` para ejecutar un contenedor a partir de la imagen etiquetada como `prodapp`. La opción `-d` indica que el contenedor debe ejecutarse en segundo plano (detached mode). `--name prod` establece el nombre del contenedor como `prod`.

**Función:** Este comando inicia un contenedor basado en la imagen `prodapp`, que fue construida en el paso anterior. El contenedor se ejecuta en segundo plano, lo que significa que no bloquea la terminal y puede continuar ejecutándose incluso después de que cierres la sesión actual.
---
**Explicación adicional:**

- Específicamente usando `-f Dockerfile` en el comando `docker build`, estás indicando explícitamente el nombre del Dockerfile que Docker debe utilizar para construir la imagen. Esto es útil cuando tienes múltiples Dockerfiles en tu proyecto y deseas asegurarte de que se use el correcto durante el proceso de construcción de la imagen.

- El comando `docker run` con la opción `-d` es común para ejecutar contenedores en segundo plano, ideal para aplicaciones de producción donde no necesitas interactuar directamente con el contenedor desde la terminal.

Estos comandos son fundamentales para el desarrollo y despliegue de aplicaciones usando Docker, asegurando que puedas construir imágenes específicas y ejecutar contenedores basados en esas imágenes de manera controlada y eficiente.
Aquí tienes la explicación de los comandos Docker proporcionados:

**Comando 123:**

```bash
$ docker run -it --rm -v /var/run/docker.sock:/var/run/docker.sock docker:19.03.12
```

**Título:** Ejecutar un contenedor Docker con acceso al socket Docker.

**Descripción:** Utiliza `docker run` para ejecutar un contenedor interactivo (`-it`) a partir de la imagen `docker:19.03.12`. La opción `--rm` indica que el contenedor debe ser eliminado después de detenerse. `-v /var/run/docker.sock:/var/run/docker.sock` monta el socket de Docker del host dentro del contenedor, permitiendo al contenedor interactuar con el daemon de Docker del host.

**Función:** Este comando es útil cuando necesitas ejecutar comandos de Docker dentro de un contenedor Dockerizado. El acceso al socket Docker desde el contenedor permite ejecutar comandos Docker como si estuvieras directamente en el host, útil para automatizar tareas de administración de Docker o ejecutar operaciones complejas.
---
**Comando 124:**

```bash
$ docker run --rm -it -v /var/run/docker.sock:/var/run/docker.sock -v $(which docker):/bin/docker wagoodman/dive:latest prodapp
```

**Título:** Ejecutar el contenedor de Dive para analizar una imagen Docker.

**Descripción:** Utiliza `docker run` para ejecutar un contenedor interactivo (`-it`) a partir de la imagen `wagoodman/dive:latest`. La opción `--rm` indica que el contenedor debe ser eliminado después de detenerse. `-v /var/run/docker.sock:/var/run/docker.sock` monta el socket de Docker del host dentro del contenedor, permitiendo a Dive interactuar con el daemon de Docker. `-v $(which docker):/bin/docker` monta el ejecutable `docker` del host dentro del contenedor, permitiendo a Dive ejecutar comandos de Docker. `prodapp` es el nombre de la imagen Docker que se analizará con Dive.

**Función:** Dive es una herramienta para explorar y analizar imágenes Docker en profundidad. Al ejecutar este comando, Dive analizará la imagen `prodapp` utilizando el acceso al daemon de Docker del host, proporcionando información detallada sobre las capas de la imagen, el uso de espacio, metadatos y más. Es una herramienta útil para entender mejor la estructura y el contenido de las imágenes Docker.
---
**Explicación adicional:**

- El montaje del socket de Docker (`/var/run/docker.sock`) dentro del contenedor es una práctica común cuando necesitas que el contenedor interactúe con Docker en el host. Esto es útil para casos de uso como la construcción de imágenes dentro de un contenedor, ejecución de contenedores secundarios, entre otros.

- El segundo comando muestra cómo puedes usar Dive dentro de un contenedor para explorar y analizar imágenes Docker. Montar el ejecutable `docker` del host dentro del contenedor permite que Dive ejecute comandos de Docker para obtener información detallada sobre las imágenes.

Estos comandos son poderosos para el desarrollo, la depuración y la gestión avanzada de imágenes Docker, proporcionando herramientas para la exploración profunda y el análisis detallado de tus contenedores y imágenes Docker.
---
