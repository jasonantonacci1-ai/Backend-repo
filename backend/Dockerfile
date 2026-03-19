FROM node:20.20.1-alpine AS builder

WORKDIR /app

ENV PORT=5000
ENV MONGODB_URL=mongodb://mongodb:27017

COPY package.json .

RUN npm install

COPY . .

EXPOSE 5000

CMD [ "node","app.js" ]

FROM node:20.20.1-alpine

WORKDIR /app

