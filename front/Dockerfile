FROM node:18.16.0-alpine

WORKDIR /usr/local/app
COPY ./ /usr/local/app/

RUN yarn
RUN npm install
RUN npm run build
 
FROM nginx:latest as production

COPY front/nginx.conf /etc/nginx/conf.d/default.conf

EXPOSE 80