FROM node:16-alpine3.12

RUN yarn global add @vue/cli
RUN mkdir -p /app
#Establece el work directory en /app
WORKDIR /app

#package.json COPY al /app
COPY package.json ./
#Actualizar dependencias con yarn
RUN yarn install
#Copia el resto de los archivos de la aplicación al /app
COPY . .

#Compila la aplicación del Vue para producción
RUN yarn build

#Usa la imagen base de Nginx
FROM nginx:alpine