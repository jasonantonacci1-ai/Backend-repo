FROM node:24-alpine

WORKDIR /app

RUN apk upgrade --no-cache

ENV MONGODB_URL=mongodb://mongodb:27017

COPY package*.json ./

RUN npm install -g npm@latest

RUN npm install --legacy-peer-deps && npm cache clean --force

COPY . .

EXPOSE 5000

CMD [ "node","app.js" ]
