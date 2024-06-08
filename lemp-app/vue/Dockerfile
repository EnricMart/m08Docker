# Etapa de construcción de la aplicación Vue.js
FROM node:16-alpine3.12 AS builder

# Instalar el CLI de Vue.js de forma global
RUN yarn global add @vue/cli

# Crear el directorio de la aplicación
WORKDIR /app

# Copiar el archivo package.json y bloquear dependencias
COPY package.json ./

# Instalar dependencias
RUN yarn install

# Copiar el resto de los archivos de la aplicación
COPY . .

# Compilar la aplicación Vue.js para producción
RUN yarn build


# Etapa final para la imagen de producción
FROM nginx:alpine

# Copiar los archivos generados de la etapa de construcción anterior a la imagen de Nginx
COPY --from=builder /app/dist /usr/share/nginx/html


