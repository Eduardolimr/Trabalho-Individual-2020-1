FROM node:lts-alpine
WORKDIR /client
COPY ./package*.json ./client/package*.json
RUN yarn install --all
COPY . .