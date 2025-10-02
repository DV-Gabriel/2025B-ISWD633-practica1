# Contenedores

### Crear un contenedor
Para crear un nuevo contenedor Docker a partir de una imagen específica, pero sin iniciarlo automáticamente. 

```
docker create --name <nombre contenedor> <nombre imagen>:<tag>
```
Crear el contenedor  **srv-web** usando la imagen nginx version alpine

<img width="551" height="61" alt="image" src="https://github.com/user-attachments/assets/2a88f9c6-69e9-447f-872d-440c5fde1ada" />

Si creas un contenedor en Docker sin asignarle un nombre específico utilizando la opción --name, Docker asignará automáticamente un nombre aleatorio al contenedor. Este nombre suele consistir en una combinación de palabras y números.  

Crear el contenedor usando la imagen hello-world

<img width="562" height="60" alt="image" src="https://github.com/user-attachments/assets/cee9b704-3d3f-4ee6-bdce-06e09c9abf48" />


### Listar los contenedores ejecutándose o no

```
docker ps -a
```

<img width="1025" height="76" alt="image" src="https://github.com/user-attachments/assets/b889c0ba-af79-4413-84ae-004bc27d5b74" />


### Para iniciar un contenedor

```
docker start <nombre contenedor o identificador>
```
Iniciar el contenedor srv-web 
```
docker start srv-web
```

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
![Ecosistema de Docker](dockerRun.PNG)

Crear y ejecutar inmediatamente el contenedor **srv-web2** usando la imagen nginx:alpine

<img width="804" height="406" alt="image" src="https://github.com/user-attachments/assets/c2378244-28f4-43ce-ba4d-11103984489f" />


**¿Qué sucede luego de la ejecución del comando?**
El contenedor se empieza a ejecutar, haciendo que la terminal sea del contenedor.

Cuando ejecutas un contenedor en primer plano sin la opción -d (modo detach), el contenedor captura la entrada estándar (stdin) del terminal, lo que significa que el terminal queda "atrapado" y no puedes introducir más comandos hasta que detengas el contenedor.

### Para crear un contenedor y ejecutarlo inmediatamente sin estar vinculados al mismo
-d: Es la opción que indica a Docker que ejecute el contenedor en segundo plano (en modo "detach").
Cuando un contenedor se ejecuta en segundo plano, Docker devuelve el control al terminal inmediatamente después de iniciar el contenedor, lo que permite al usuario seguir ejecutando otros comandos en el mismo terminal sin que el contenedor detenga la interacción.

```
docker run -d --name <nombre contenedor> <nombre imagen>:tag
```
Crear y ejecutar inmediatamente el contenedor **srv-web3** en modo detach usando la imagen nginx:alpine

<img width="552" height="68" alt="image" src="https://github.com/user-attachments/assets/c58c6ccf-adda-4dbd-a19b-df592cf18cba" />


### Para eliminar un contenedor

```
docker rm <nombre contenedor>
```
Eliminar el contenedor que se creó a partir de la imagen hello-world 

<img width="418" height="58" alt="image" src="https://github.com/user-attachments/assets/9cf48f9d-85bf-4f26-9af8-1d3af5d3e77e" />

Verificar que el contenedor que se eliminó

<img width="999" height="94" alt="image" src="https://github.com/user-attachments/assets/7f0421f0-757e-43f2-acdb-8603d02e18a8" />


### Para eliminar un contenedor que esté ejecutándose

```
docker rm -f <nombre contenedor>
```
Eliminar el contenedor **srv-web3** 

<img width="365" height="57" alt="image" src="https://github.com/user-attachments/assets/72e93a2f-219f-4dbb-91d7-6fb8f9534568" />

Verificar que el contenedor que se eliminó

<img width="1007" height="84" alt="image" src="https://github.com/user-attachments/assets/331281d0-9c80-4dbd-8a8e-8bbe49d9cd3f" />


### Para inspecionar un contenedor 

Inspeccionar el contenedor **srv-web** 

<img width="1016" height="478" alt="image" src="https://github.com/user-attachments/assets/d896b926-bea4-4988-baae-3759d57797e0" />

