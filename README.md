# Laboratorio Cloud - Render auto

Preparamos el archivo Dockerfile y .dockerignore. Abordamos el Dockerfile con un enfoque multietapa:

- En la etapa base, declaramos la imagen base (node:24-alpine) y preparamos el directorio de trabajo.
- En la etapa de construcción, copiamos todo el código fuente, instalamos dependencias y ejecutamos la build
- En la etapa de release, definimos la variable de entorno, copiamos los archivos estáticos del dist, los archivos necesarios del servidor, instalamos las dependencias de producción y definimos el comando de inicio

Subimos el proyecto a nuestro repositorio de Github

Entramos a Render y desplegamos un Web Service a través de un repositorio de Github
