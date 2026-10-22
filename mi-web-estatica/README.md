# Web sobre virtualización (PaaS en Render con Docker)

Web estática servida con Nginx dentro de un contenedor Docker.

## Probar en local
    docker build -t web-virtualizacion .
    docker run --rm -p 8080:10000 web-virtualizacion
Abre http://localhost:8080

## Desplegar en Render
1. Sube esta carpeta a un repositorio de GitHub (index.html, Dockerfile, nginx.conf.template, .dockerignore en la raíz).
2. En render.com: New > Web Service > conecta el repositorio.
3. Language: Docker. Instance Type: Free. Deja la raíz y el Dockerfile por defecto.
4. Pulsa Create Web Service. Render construye la imagen y te da una URL https://<nombre>.onrender.com.

Cada git push a la rama principal redespliega la web automáticamente.
Nota: en el plan gratuito el servicio se duerme tras 15 minutos sin visitas y tarda unos segundos en despertar.
