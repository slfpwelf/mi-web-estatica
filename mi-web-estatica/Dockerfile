FROM nginx:1.27-alpine

# Render asigna el puerto en la variable PORT (10000 por defecto)
ENV PORT=10000

# La plantilla se procesa al arrancar y sustituye ${PORT}
COPY nginx.conf.template /etc/nginx/templates/default.conf.template
COPY index.html /usr/share/nginx/html/index.html

EXPOSE 10000
