## Build
FROM node:16-alpine AS builder
# Create app directory
WORKDIR /app
# Install app dependencies
# A wildcard is used to ensure both package.json AND package-lock.json are copied
COPY package*.json ./app
RUN npm ci
RUN npm install -g @ionic/cli
# Bundle app source
COPY . .
RUN ionic build
## Run 
FROM nginx:alpine
#COPY www /usr/share/nginx/html
COPY --from=builder  /app/www /usr/share/nginx/html