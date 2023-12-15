FROM node:21-alpine  

EXPOSE 80 3000

WORKDIR /usr/src/app

RUN apk add --update tini

RUN mkdir -p /usr/src/app

COPY package.json package.json

RUN npm install && npm cache clean

COPY . .

CMD [ "tini", "--", "node", "./bin/www" ]