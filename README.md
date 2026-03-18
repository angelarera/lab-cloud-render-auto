# Laboratorio Cloud - Render auto

Preparamos el archivo Dockerfile y .dockerignore. Abordamos el Dockerfile con un enfoque multietapa:

- En la etapa base, declaramos la imagen base (node:24-alpine) y preparamos el directorio de trabajo.
- En la etapa de construcción, copiamos todo el código fuente, instalamos dependencias y ejecutamos la build
- En la etapa de release, definimos la variable de entorno, copiamos los archivos estáticos del dist, los archivos necesarios del servidor, instalamos las dependencias de producción, exponemos el puerto y definimos el comando de inicio

Generamos con Docker nuestra imagen usando el comando `docker build`

El siguiente paso será subir la imagen al registry de DockerHub. Para ello tenemos que hacer login, renombrar nuestra imagen de forma que apunte a nuestro nombre de usuario (`angelarera/my-app:1` para mi caso), y la desplegamos con `docker push`
