# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/38ec0ec7-a0ad-4525-81fb-b2c141e7d59f)

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/38874574-eb38-41db-9291-6fd7978a9f03)


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
# COMPLETAR

![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/4013a8eb-4b2e-44b4-a030-e41607622730)


### Listar los contenedores ejecutándose
```
docker ps 
docker ps | grep <nombre contenedor>
```

### Para detener un contenedor

```
docker stop <nombre contenedor>
```

### Para crear un contenedor y ejecutarlo inmediatamente

```
docker run --name <nombre contenedor> <nombre imagen>:<tag>
```
![Ecosistema de Docker](imagenes/dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/e995fe0a-9f8e-421e-bdd1-79d73dad5ffa)

**¿Qué sucede luego de la ejecución del comando?**
# COMPLETAR  
# Inicia el contenedo ejecutandose y solo se queda iniciandose.
Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/5cd00a7b-a501-489a-8859-ee291d1cf621)

### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/56a83d62-073c-47a6-bc77-20ffaaba7581)

Verificar que el contenedor que se eliminó
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/cdd3e51a-6b4c-49fa-acfd-2aff325316ef)
# Se ha eliminado el que hacia referencia al contenedor 3c...
### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/5b5893a0-f6e8-4de2-8326-0a926edfed3f)

Verificar que el contenedor que se eliminó
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/41e8b0d1-dadd-43be-97e4-cb375c90010c)

### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 
# COMPLETAR
![image](https://github.com/Cristian-Zambrano/2024A-ISWD633-GR2/assets/94475992/c22d7218-ad83-4a68-ab87-a6660a4e7862)
