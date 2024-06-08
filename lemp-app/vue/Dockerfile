FROM node:16-alpine3.12

RUN npm install @vue/cli -g
RUN mkdir -p /app

#Establece el work directory en /app
WORKDIR /app

#package.json COPY al /app
COPY package.json ./

#Copia el resto de los archivos de la aplicación al /app
COPY . .


#Usa la imagen base de Nginx
FROM nginx:alpine


RUN npm install

EXPOSE 7500 

CMD [ "npm","run","serve","--","--port","7500"]