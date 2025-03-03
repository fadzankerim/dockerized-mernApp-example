ARG NODE_VERSION=22.13.1

FROM node:${NODE_VERSION}-alpine

RUN addgroup app && adduser -S -G app app


WORKDIR /app

COPY package*.json ./

# change ownership of the /app directory to the app user
USER app

RUN npm install

COPY . . 

EXPOSE 8000 

CMD npm start