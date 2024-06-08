FROM node:16-alpine3.12

#Establece el work directory en /app
WORKDIR /app

#package.json y yarn.lock COPY al /app
COPY package.json yarn.lock ./

RUN yarn install

#Copia el resto de los archivos de la aplicación al /app
COPY . .

RUN yarn install

RUN yarn global add

EXPOSE 7500 

CMD [ "npm","run","serve","--","--port","7500"]