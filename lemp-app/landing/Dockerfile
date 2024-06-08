FROM node:16-alpine3.12

# Crear directorio de la aplicación
RUN mkdir -p /app

# Establecer directorio de trabajo
WORKDIR /app

# Copiar archivos package*.json
COPY ./package*.json .

# Instalar dependencias
RUN npm install

# Cambiar el propietario del directorio /app al usuario 'node'
RUN chown -R node:node /app

# Cambiar al usuario 'node' para ejecutar la aplicación
USER node

# Comando para iniciar la aplicación Vue.js
CMD [ "npm", "run", "serve", "--", "--port", "7500" ]
