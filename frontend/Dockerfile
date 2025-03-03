ARG NODE_VERSION=22.13.1

FROM node:${NODE_VERSION}-alpine

RUN addgroup app && adduser -S -G app app

USER app

WORKDIR /app

COPY package*.json ./

RUN npm install

COPY . .

EXPOSE 5173

CMD npm run dev
