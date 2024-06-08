FROM node:16-alpine3.12

# Establece el directorio de trabajo en /app
WORKDIR /app

# Copia package.json y yarn.lock al directorio de trabajo
COPY package.json yarn.lock ./

# Instala las dependencias
RUN yarn install

# Copia el resto de los archivos de la aplicación al directorio de trabajo
COPY . .

# Instala http-server globalmente (si es necesario)
RUN yarn global add http-server

# Expone el puerto 8080 para la aplicación Vue.js
EXPOSE 8080

# Comando para ejecutar la aplicación Vue.js
CMD ["http-server", "dist"]
