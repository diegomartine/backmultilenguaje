FROM node:18.15.0-slim

RUN mkdir /app
WORKDIR /app

ENV JSON_SERVER_VERSION=0.17.3

RUN npm install -g json-server@${JSON_SERVER_VERSION}
COPY package.json package-lock.json ./
RUN npm ci --only="prod"

COPY ./db.json ./routes.json ./server.sh ./

EXPOSE 80
CMD [ "./server.sh" ]
