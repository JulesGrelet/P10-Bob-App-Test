FROM node:latest as build

WORKDIR /usr/local/app
COPY ./ /usr/local/app/

RUN yarn
RUN npm run build
 
FROM nginx:latest as production

EXPOSE 80