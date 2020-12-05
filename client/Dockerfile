FROM node:15
WORKDIR /client
COPY ./package*.json ./client/package*.json
RUN yarn install
COPY . .
RUN yarn dev