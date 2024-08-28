# Documentación

## Creando docker red

1. Crear red docker: **`docker network create nombre_docker_red`**
2. Listar Todas las Redes Docker: **`docker network ls`**
3. Obtener Detalles de una Red Específica: **`docker network inspect nombre_red`**
4. Eliminar una Red Docker: **`docker network rm nombre_red`**

## Comandos Docker

1. Crear contenedor: **`docker run --name nombre_docker --network nombre_red -it ubuntu /bin/bash`**
2. Añadirlo a una red Docker: **`docker network connect nombre_red nombre_docker`**
3. Listar Contenedores Activos: **`docker ps`**
4. Listar todos los contenedores: **`docker ps -a`**
5. Buscar el Contenedor por Nombre o ID: **`docker ps -a | grep nombre_parcial`**
6. Volver a Iniciar un Contenedor Detenido: **`docker start nombre_contenedor`**
7. Acceder al Contenedor: **`docker exec -it nombre_contenedor /bin/bash`**
8. Detener un Contenedor por Nombre o ID: **`docker stop nombre_contenedor`**
9. Detener Todos los Contenedores: **`docker stop $(docker ps -q)`**
10. Eliminar un Contenedor: **`docker rm nombre_contenedor`**
11. Eliminar Todos los Contenedores Detenidos: **`docker container prune`**
12. Eliminar una Imagen Docker: **`docker rmi nombre_imagen`**
13. Desconectar el Contenedor de la Red Actual: **`docker network disconnect nombre_red nombre_contenedor`**
14. Conectar el Contenedor a la Nueva Red: **`docker network connect nombre_red_nueva nombre_contenedor`**
