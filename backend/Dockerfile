FROM node:18-alpine

WORKDIR /app

ENV MONGODB_URL=mongodb://mongodb:27017

COPY package*.json ./

RUN npm install --legacy-peer-deps && npm cache clean --force

COPY . .

EXPOSE 5000

CMD [ "node","app.js" ]


