FROM node:14-alpine

WORKDIR /app

RUN apk update && \
  apk add git python make g++ --no-cache && \
  npm i -g @vue/cli@4.0.5 vue@2.6.11 create-nuxt-app@3.0.0
