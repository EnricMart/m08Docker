
FROM node:16-alpine3.12

#creamos carpeta app 
RUN mkdir -p /app
#entramos en la carpeta app
WORKDIR /app
#copiamos el package json en app
COPY ./package*.json .
#actualizamos dependencias de node.js
RUN npm install
#indicamos el puerto
EXPOSE 7500
#runeamos el servidor 7500
CMD [ "npm", "run", "serve", "--", "--port", "7500" ]
