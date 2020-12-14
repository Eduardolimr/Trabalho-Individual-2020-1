FROM node:15
WORKDIR /client
COPY ./package*.json ./client/package*.json
RUN yarn install
RUN yarn global add @vue/cli@4.4.6
COPY . .
RUN yarn dev